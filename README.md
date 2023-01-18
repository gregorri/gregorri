```Python
#!/usr/bin/python3
# -*- coding: utf-8 -*-


class aboutMe:
    def __init__(self, name, role):
        self.name = name
        self.role = role
        self.projects = []
    
    def sayHi(self):
        print("Hi everyone 👋")

    def addProject(self, project):
        self.projects.append(project)

    def createReadme(self):
        with open("README.md", "w") as f:
            f.write("Hi there! My name is **{}** and I am a **{}**.\n".format(self.name, self.role))
            f.write("# Skills\n")
            f.write("- Python\n,- JavaScript\n,- HTML/CSS\n\n")
            f.write("# Projects\n")
            for project in self.projects:
                f.write("- {}\n".format(project))
            f.write("# Contact\n")
            f.write("Feel free to contact me at [email](mailto:{}) or [LinkedIn](https://www.linkedin.com/in/{}/).\n".format(self.email, self.linkedin))

me = aboutMe("Greg", "IT Technician")
me.addProject("[Project 1](https://github.com/username/project1)")
me.addproject("[Project 2](https://github.com/username/project2)")
me.createReadme()
```
