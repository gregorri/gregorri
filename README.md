```Python
#!/usr/bin/python3
# -*- coding: utf-8 -*-

class AboutMe:
    def __init__(self, name, role, languages, email, linkedin):
        self.name = name
        self.role = role
        self.languages = languages
        self.email = email
        self.linkedin = linkedin
        self.projects = []
        
    def addProject(self, project):
        self.projects.append(project)

    def createReadme(self):
        with open("README.md", "w") as f:
            f.write("# Introduction\n")
            f.write("Hi there! My name is **{}** and I am a **{}**.\n".format(self.name, self.role))
            f.write("I am fluent in the following languages: {}.\n".format(", ".join(self.languages)))
            f.write("# Skills\n")
            f.write("- Python\n- mongoBD\n- html5\css3\n- linux\n- git\n")
            f.write("# Projects\n")
            for project in self.projects:
                f.write("- {}\n".format(project))
            f.write("# Contact\n")
            f.write("Feel free to contact me at [email](mailto:{}) or [LinkedIn](https://www.linkedin.com/in/{}/).\n"
            .format(self.email, self.linkedin))

me = AboutMe("Usachi Grigore", "IT Technician", ["ro_RO", "it_IT", "ru_RU", "en_US"], "qgrisa@gmail.com", "gregurs")
me.addProject("[Project 1](https://github.com/username/project1)")
me.addProject("[Project 2](https://github.com/username/project2)")
me.createReadme()
```
