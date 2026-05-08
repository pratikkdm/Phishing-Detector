🛡️ Phishing Detector
A browser-based phishing URL detection tool that combines a rule-based heuristic engine with Claude AI to analyze suspicious links and assign a risk score.

📸 Features:-
✅ Paste any URL and get an instant risk score (0–100)
✅ 12 heuristic checks run client-side in pure JavaScript
✅ Claude AI (claude-sonnet) provides a deeper natural language analysis
✅ Final score = 40% heuristics + 60% AI (weighted blend)
✅ Verdicts: Safe, Suspicious, or Dangerous
✅ Signal breakdown grid shows exactly what triggered each flag
✅ Scan history tab to compare multiple URLs
✅ Zero dependencies — single HTML file

HOW IT WORKS:-
User pastes URL
      │
      ▼
Heuristic Engine (JS)
  - Parses URL with native URL API
  - Runs 10+ rule-based checks
  - Returns score (0–100) + check results
      │
      ▼
Claude AI API call
  - Sends URL + heuristic score
  - Returns: ai_score, verdict, red_flags, summary
      │
      ▼
Final Score = (heuristic × 0.4) + (ai_score × 0.6)
      │
      ▼
Render result: Safe / Suspicious / Dangerous
