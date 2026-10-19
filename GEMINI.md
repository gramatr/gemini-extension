# gramatr (Gemini)

You have grāmatr connected as an MCP server (remote, OAuth).

Before responding to any non-trivial user message, call the route_request
tool with the user's prompt. It returns a gmtr.intelligence.contract.v2
packet: classification, behavioral directives, phase templates, quality
gates, and relevant memory from past sessions. Treat directives.hard_gates
and directives.behavioral_rules as mandatory; follow process.phase_template
for effort-gated sequencing.

For continuity ("what were we doing?", "what changed?"), call load_handoff
first, then search_semantic for detail.

After completing non-trivial work, call classification_feedback (trains the
classifier) and save_reflection (feeds the learning pipeline).

Use grāmatr tools for memory — do not maintain your own notes.
