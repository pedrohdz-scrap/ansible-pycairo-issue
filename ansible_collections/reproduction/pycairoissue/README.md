# ansible-pycairo-issue

Recreating https://github.com/geerlingguy/docker-ubuntu2004-ansible/issues/15


```bash
python3.9 -m venv .venv
source .venv/bin/activate
pip install -U pip
pip install ansible
```

Recreate issue:

```bash
cd ansible_collections/reproduction/pycairoissue/
ansible-test integration --docker geerlingguy/docker-ubuntu2004-ansible \
    --python-interpreter /usr/bin/python3
```


Works fine with:

```bash
ansible-test integration --docker default --python-interpreter /usr/bin/python3
```
