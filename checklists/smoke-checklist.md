# Smoke Checklist

## Web Application

- [ ] Main page opens without server errors.
- [ ] Header, footer, and main navigation are displayed.
- [ ] Login page opens.
- [ ] User can log in with valid credentials.
- [ ] User can log out.
- [ ] Main user dashboard opens after login.
- [ ] Key buttons and links are clickable.
- [ ] Forms show validation messages for empty required fields.
- [ ] No critical errors are displayed in browser console.
- [ ] Page is usable on desktop and mobile viewport.

## Mobile Application

- [ ] Application starts without crash.
- [ ] Splash screen is displayed correctly.
- [ ] Login screen opens.
- [ ] User can log in with valid credentials.
- [ ] Bottom navigation works.
- [ ] Main screens are opened without endless loaders.
- [ ] Push permission dialog does not block core flows.
- [ ] Application handles offline mode with clear message.
- [ ] User can log out.

## API

- [ ] Health endpoint returns successful response.
- [ ] Authorized endpoint rejects request without token.
- [ ] Authorized endpoint accepts request with valid token.
- [ ] Invalid request body returns validation error.
- [ ] Response structure matches API documentation.
- [ ] Response time is within accepted limit.
