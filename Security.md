## Security Considerations

### Security Vulnerability

#### Hardcoded Secrets:

A common security vulnerability in software development is hardcoding secrets such as API keys, passwords or access tokens directly in source code.

For demonstration purposes, `security_example.py` contains a fake API key directly in the source code. This demonstrates what should not be done in a real application.

If a real credential were hardcoded and the repository became publicly accessible or was accessed by an unauthorized person, the credential could be exposed and potentially misused.

### Mitigation:

The secure approach is to keep secrets outside the source code and provide them through environment variables or a secure secrets management system.

The secure example in `security_example_secure.py` retrieves the value from an environment variable:

import os

API_KEY = os.environ.get("API_KEY")
