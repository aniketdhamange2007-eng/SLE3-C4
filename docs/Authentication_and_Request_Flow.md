
---

## 6. `docs/Authentication_and_Request_Flow.md`

```markdown
# Authentication and Request Flow

## 1. Authentication Status

The Basic AI Personal Assistant currently has no application-level authentication.

The application does not contain:

- Username/password login
- Password storage
- API keys
- OAuth
- JWT
- Refresh tokens
- Session tokens
- Authentication middleware
- External identity provider

---

# 2. Credential Handling

No user credentials are collected by the Python application.

There is no username → password → authentication server flow.

Therefore, there is no password database or credential storage in the current system.

---

# 3. Token Handling

The application does not generate, store, validate or refresh authentication tokens.

There are no:

- Access Tokens
- Refresh Tokens
- JWTs
- Session Tokens
- OAuth Tokens

---

# 4. Actual Request Flow

```text
User
  ↓
run_agent()
  ↓
input(command)
  ↓
get_response(command)
  ↓
Command Normalization
  ↓
Command Matching
  ↓
Rule Handler
  │
  └── Calculator Request
          ↓
     calculate(expression)
          ↓
       Response
          ↓
    print(response)
          ↓
        User
