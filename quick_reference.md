# Quick Reference Guide

One-page reference for common tasks and commands.

---

## 🚀 Quick Commands

### Run Reports
```bash
python main.py morning    # Morning brief
python main.py midday     # Midday update
python main.py evening    # Evening wrap
```

### Check System Status
```bash
# Cloud Run
gcloud run services list

# View logs
gcloud logging read "resource.type=cloud_run_revision" --limit=20

# Check scheduler jobs
gcloud scheduler jobs list
```

---

## 📅 Turkish Economic Calendar 2025

### CBT (TCMB) Meetings
Jan 23, Feb 20, Mar 20, Apr 24, May 22, Jun 19, Jul 24, Aug 21, Sep 18, Oct 23, Nov 20, Dec 25

### Inflation Reports
Jan 3, Feb 3, Mar 3, Apr 3, May 5, Jun 3, Jul 3, Aug 4, Sep 3, Oct 3, Nov 3, Dec 3

---

## 📊 Key Metrics

### Alert Severity Levels
1. **Info** → Log only
2. **Notice** → Email
3. **Warning** → Email + Slack
4. **Critical** → Email + Slack + SMS
5. **Emergency** → All channels + Voice

### Macro Regimes
- **Goldilocks**: Strong growth + Low inflation → Buy equities
- **Inflationary**: High inflation + Growth → Commodities, TIPS
- **Stagflation**: High inflation + Weak growth → Gold, cash
- **Deflationary**: Low inflation + Weak growth → Bonds, safe havens
- **Reflation**: Rising inflation + Improving growth → Cyclicals

---

## 🇹🇷 Turkish Dividend Stocks

Top monitored stocks: **EREGL, FROTO, TUPRS, DOAS, TTRAK, ISMEN, ENJSA**

---

## 🔧 Configuration

### Environment Variables
```bash
FINNHUB_API_KEY=your_key
OPENAI_API_KEY=your_key
PERPLEXITY_API_KEY=your_key
SLACK_WEBHOOK_URL=your_webhook (optional)
```

### GCP Secrets
```bash
# Update secret
echo -n "new_value" | gcloud secrets versions add SECRET_NAME --data-file=-

# View secret
gcloud secrets versions access latest --secret=SECRET_NAME
```

---

## 📈 Portfolio Metrics

### Risk Metrics
- **Sharpe Ratio**: (Return - Risk-free rate) / Volatility
  - \> 1.0 = Excellent
  - 0.5-1.0 = Good
  - < 0.5 = Poor

- **Max Drawdown**: Largest peak-to-trough decline
  - < 10% = Low risk
  - 10-20% = Moderate risk
  - \> 20% = High risk

- **VaR 95%**: Potential 1-day loss with 95% confidence

---

## 🚨 Common Issues

### Issue: Cloud Run 503
**Fix**: Increase max instances or concurrency

### Issue: Scheduler job failed
**Fix**: Check service URL and IAM permissions

### Issue: Missing API data
**Fix**: Verify API keys in Secret Manager

---

## 💰 Cost Breakdown

- **Cloud Run**: ~$2/month
- **Scheduler**: ~$0.30/month
- **Firestore**: ~$5/month
- **APIs**: ~$70/month
- **Total**: ~$75-80/month

---

## 📞 Getting Help

1. Check `deployment_guide.md` for setup issues
2. Review `ultimate_investor_guide.md` for usage
3. Check system logs in Cloud Logging
4. Review code comments in module files

---

## 🎯 Success Checklist

- [ ] Deployment successful (all tests passing)
- [ ] Scheduler jobs running (3 daily jobs)
- [ ] Alerts configured (Slack/Email)
- [ ] API keys working (Finnhub, OpenAI)
- [ ] Receiving daily reports
- [ ] Monitoring dashboard set up

---

**Need more details? See `ultimate_investor_guide.md`**
