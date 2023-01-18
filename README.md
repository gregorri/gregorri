```Python
#!/usr/bin/python
# -*- coding: utf-8 -*-


def create_readme():
    with open("README.md", "w") as f:
        f.write("# My Project\n")
        f.write("This is my project.\n")

if __name__ == "__main__":
    create_readme()
```
