# API
This is for multiple purposes.

## Auth
This is authentication purposes only.

### Usage
Bash
```bash
curl -s https://akashisgreat.github.io/api/auth.json
```

Python
```python
import requests
def auth(auth_url,value_name):
    try:
        response = requests.get(auth_url)
        response.raise_for_status()  
        response_data = response.json()
        if response_data.get(value_name):
            pass
        else:
            print("Auth Failed.")
            exit()
    except (requests.RequestException, ValueError) as e:
        print(f"An error occurred: {e}")
        exit()
auth("https://akashisgreat.github.io/api/auth.json","test_true")
```
