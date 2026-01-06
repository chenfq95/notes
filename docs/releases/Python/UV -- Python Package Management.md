# Manage Python Version
installing the latest python version
```bash
uv python install
```
installing a special python version
```bash
uv python install 3.13
```
reinstalling python
```bash
uv python install --reinstall
```
listing all python versions installed locally
```bash
uv python list
```
upgrading a python version
```bash
uv python upgrade 3.12
```
uninstalling a python version
```bash
uv python uninstall 3.12
```
pining the current project to use a special python version
```bash
uv python pin 3.12
```
# Running Scripts

creating a python script
```bash
uv init --script example.py
```
adding dependencies to the script
```bash
uv add --script example.py 'rich' 'requests<3'
```
run example.py
```bash
uv run example.py
```
using a shebang to create an executable file
```bash
#!/usr/bin/env -S uv run --script

print("Hello world from example.py")
```
locking script dependencies
```bash
uv lock --script example.py
```
# Using tools
invoking ruff without installing it 
```
uvx ruff # exactly equals 'uv tool run ruff'
```
providing args after the tool name
```bash
uvx pycowsay hello from uv
```
invoking a command provided by the special tool
```bash
uvx --from httpip http
```
installing tools
```
uv tool install ruff
ruff --version
```
upgrading tools
```bash
uv tool upgrade ruff
```
# Working on projects
creating a new project
```bash
uv init hello_world
```
initializing a existing project
```bash
uv init 
```
adding a package as a dependency 
```bash
uv add requests
```
migrating from a `requirements.txt`
```bash
uv add -r requirements.txt -c constraints.txt
```
removing a package
```bash
uv remove requests
```
running a command
```bash
uv add flask # package added before
uv run -- flask run -p 3000
```
running a script
```
uv run example.py # will use the project environment
```
