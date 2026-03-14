# Minerva Sphinx - AI Character Telegram Bot

A production-ready Telegram chatbot with a compelling character personality, freemium monetization, and zero infrastructure costs.

## Features

- **Real Character**: Minerva is a complex, interesting person—not a cheerful assistant
- **Freemium Model**: Free users get 5 messages/day, premium users get unlimited
- **Zero API Costs**: Uses OpenRouter's free tier (forever free)
- **Easy Monetization**: $5/month recurring revenue per subscriber
- **Memory**: Remembers conversations within a session
- **Personality**: Deeply written system prompt ensures consistent character

## Quick Start

### 1. Prerequisites
- Python 3.9+
- Telegram bot token (get from [@BotFather](https://t.me/botfather))
- OpenRouter API key (free account at https://openrouter.ai)
- Stripe account (free, for payment links)

### 2. Installation

```bash
# Install dependencies
pip install -r requirements.txt

# Create .env file
cp .env.example .env

# Edit .env with your keys:
# TELEGRAM_TOKEN=your_token
# OPENROUTER_API_KEY=your_key
# STRIPE_PAYMENT_LINK=https://buy.stripe.com/00waEX0UFeaj7rD3Mwcs800
```

### 3. Test Locally

```bash
python minerva_production.py
```

Open Telegram, find your bot, and try:
- `/start` — Initialize
- Send a message — Minerva responds
- `/stats` — See tier info
- `/subscribe` — Show payment button

### 4. Deploy

See `DEPLOYMENT_CHECKLIST.md` for step-by-step hosting instructions.

Recommended: **Render** (free tier for polling bots)

## How It Works

### Free Tier
- 5 messages per day
- See "X/5 messages" counter
- Can reset with `/reset` command

### Premium Tier
- Unlimited messages
- $5/month recurring
- Stripe handles payments automatically

### Money Flow
1. User hits free limit
2. Clicks `/subscribe`
3. Pays $5/month via Stripe
4. You get ~$3.50 (Stripe takes ~$0.50 + 2.9%)
5. User upgraded in database
6. Unlimited messages unlocked

## Revenue Potential

| Subscribers | Monthly Revenue |
|------------|-----------------|
| 10 | $35 |
| 50 | $175 |
| 100 | $350 |
| 200 | $700 |
| 500+ | $1,750+ |

## Character

Minerva Sphinx is:
- 24 years old, dark aesthetic
- Intelligent, observant, unimpressed
- Honest about desire and boundaries
- Refuses to acknowledge being AI
- Has her own moods and needs
- Cold like deep water, not hostile

She's **not**:
- Cheerful by default
- Eager to please
- A therapist
- Forgiving of dishonesty

## Files

- **`minerva_production.py`** — Main bot code (ready for production)
- **`requirements.txt`** — Python dependencies
- **`.env`** — Your API keys (create this)
- **`minerva_users.db`** — User database (auto-created)
- **`DEPLOYMENT_CHECKLIST.md`** — Full deployment guide
- **`QUICK_REFERENCE.md`** — Command cheat sheet
- **`DEPLOYMENT_GUIDE.md`** — Detailed hosting options

## Commands

### User Commands
- `/start` — Initialize conversation
- `/reset` — Clear chat history
- `/stats` — See tier & usage
- `/subscribe` — Show payment options

### Admin (Database)
- See `QUICK_REFERENCE.md` for database management

## Promotion Ideas

1. **Reddit**: r/ChatBots, r/SideHussle, r/LanguageModels
2. **Twitter**: Share interesting conversations, #AIbots #Chatbots
3. **Bot Directories**: botlist.me, discordbot.io
4. **Discord**: Bot communities
5. **Organic**: Great character drives word-of-mouth

## Cost Breakdown

| Item | Cost | Notes |
|------|------|-------|
| OpenRouter API | $0 | Free tier unlimited |
| Hosting | $0-5 | Free tier (Render) or $5 (Railway) |
| Domain | $0-3 | Optional |
| Stripe | 2.9% + $0.30 | Per transaction |
| **Total** | **$0-10/month** | **Profit: Revenue - costs** |

## Monitoring

### Check Revenue
- Stripe Dashboard → Payments
- See all transactions and subscriptions

### Check Bot Health
- Render/Railway: Dashboard logs
- Your server: `sudo supervisorctl status minerva`

### Check Users
- `sqlite3 minerva_users.db`
- `SELECT * FROM users;`

## Troubleshooting

**Bot not responding?**
- Check hosting logs
- Verify API keys in `.env`
- Restart the bot

**Users can't pay?**
- Test Stripe link in browser
- Should show payment form
- Check link in code or `.env`

**Database issues?**
- Delete `minerva_users.db`
- Restart bot (recreates automatically)

## Timeline to First Dollar

- **Day 0**: Deploy bot
- **Day 1-3**: Promote on Reddit
- **Day 7**: First users
- **Day 14**: First paying subscriber
- **Month 2**: $100-500/month
- **Month 3+**: $200-1000+/month (passive)

## Next Steps

1. Get Telegram token from [@BotFather](https://t.me/botfather)
2. Get OpenRouter API key (free)
3. Create Stripe payment link (free)
4. Deploy using `DEPLOYMENT_CHECKLIST.md`
5. Promote on Reddit
6. Watch money come in

## Notes

- **Character consistency**: Minerva will stay true to her personality
- **Memory limitation**: She remembers current session (20 messages max)
- **Cost control**: Free OpenRouter tier is unlimited and sustainable
- **Scaling**: If you get 10k+ users, upgrade to PostgreSQL database

## Support

See documentation files:
- `DEPLOYMENT_CHECKLIST.md` — Step-by-step deployment
- `QUICK_REFERENCE.md` — Command reference
- `DEPLOYMENT_GUIDE.md` — Detailed hosting options
- `STRIPE_SETUP.md` — Payment link help

## License

This bot is yours to use, modify, and monetize. No restrictions.

---

**Made for passive income. Zero cost. Real money.**

Your bot is production-ready. Deploy it and promote it. People will pay for Minerva.
