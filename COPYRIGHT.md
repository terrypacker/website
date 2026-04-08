## File Copyright Headers
Adding file headers using `licenseheaders` python tool.

### Setup
```bash
python3 -m venv .venv
source .venv/bin/activate
pip install licenseheaders
```
You will then likely need to move the templates directory so the tool
can find them.  Check the python folder version first.
```bash
ls .venv/lib
```


```bash
mv .venv/templates .venv/lib/python3/site-packages
```

#### Add Headers to index.html
```bash
source .venv/bin/activate
python3 -m licenseheaders -f index.html -t apache -cy -o 'Terry Packer' -n 'Terry Packer'\''s Work' -u 'www.terrypacker.com'
```

#### Add Headers to assets
```bash
source .venv/bin/activate
python3 -m licenseheaders -d assets -t apache -cy --additional-extensions 'html=.htm' -o 'Terry Packer' -n 'Terry Packer'\''s Work' -u 'www.terrypacker.com'
```

