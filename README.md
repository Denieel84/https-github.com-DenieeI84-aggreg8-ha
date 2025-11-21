# Aggreg8 Home Assistant Integration (HACS release)
This package contains a custom integration for Home Assistant that uses Aggreg8 (Hungarian AISP) to fetch bank account balances and transactions.

## Features
- Balance sensor per account
- Transactions sensor per account (stores latest transactions as attributes)
- Multiple account support (comma-separated IDs)
- Config flow with account discovery (dropdown when API supports it)
- Token refresh using refresh_token

## Installation (HACS)
1. Add repository to HACS (as custom) or install manually.
2. Restart Home Assistant.
3. Go to Settings → Devices & Services → Add Integration → search for "Aggreg8".
4. Provide Client ID, Client Secret, Refresh Token and choose account(s).

## Notes
- This integration is a minimal reference implementation. Verify API endpoints and responses with Aggreg8 documentation.
- If Aggreg8 returns a new refresh_token during refresh, the integration updates it in-memory but does not persist it automatically. Persisting requires storage API code enhancements.
