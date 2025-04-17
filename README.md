# gpushare

Python client for the GPU Share service.

## Installation

```bash
pip install gpushare
```

## Quickstart
```python
from gpushare import GPUShareClient, AuthenticationError, APIError

client = GPUShareClient("https://gpushare.srimanhq.com")

# 1. Authenticate (OTP flow):
client.login("you@example.com", "yourpassword", "8bit string")
# then enter the OTP when prompted

# or, if you already have a token:
client.set_api_token("YOUR_API_TOKEN")

# 2. Pick a GPU
client.select_gpu(1)

# 3. Execute code
output = client.execute_code("print('Hello from GPU!')")
print(output)
```
