### env variables
to read env variables from `.env` file of the repo:
- we intall this:
```
pip install python-dotenv
```
```python
from dotenv import load_dotenv
# we use dotenv to use os.getenv() instead of os.environ[]
# and read from '.env' in current folder instead of '/etc/environment'
# more guide:
# https://dev.to/jakewitcher/using-env-files-for-environment-variables-in-python-applications-55a1
load_dotenv()
os.getenv('TOKEN')
```
