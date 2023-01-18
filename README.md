```Python
#!/usr/bin/python3
# -*- coding: utf-8 -*-


def create_readme(name, age, job, company, studies):
    with open("README.md", "w") as f:
        f.write("# About Me\n")
        f.write("My name is {} and I am {} years old.\n".format(name, age))
        f.write("I currently work as an {} at {}.\n".format(job, company))
        f.write("I am also studying {}.\n".format(studies))

if __name__ == "__main__":
    create_readme("23 years old boy", "IT Technician", "Yashi Italia", "programming with python")
```
