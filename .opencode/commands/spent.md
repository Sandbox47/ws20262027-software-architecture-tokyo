---
description: Show OpenRouter credit balance (total, used, remaining)
---

!`curl -s -H "Authorization: Bearer $OPENROUTER_API_KEY" https://openrouter.ai/api/v1/credits 2>/dev/null | python3 -c "import sys,json; d=json.load(sys.stdin)['data']; t=float(d['total_credits']); u=float(d['total_usage']); print('OpenRouter credits: total \$%.2f  used \$%.2f  remaining \$%.2f' % (t, u, t-u))" 2>/dev/null || echo "Could not fetch OpenRouter credits. Set OPENROUTER_API_KEY (management key) via: opencode service set env OPENROUTER_API_KEY <key>"`
