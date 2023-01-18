```Python
#!/usr/bin/python3
# -*- coding: utf-8 -*-


class SoftwareEngineer:

    def __init__(self, name, role, languages, email, linkedin):
        self.name = name
        self.role = role
        self.languages = languages
        self.email = email
        self.linkedin = linkedin
        self.projects = []

    def add_project(self, project):
        self.projects.append(project)

    def say_hi(self):
        print("Thanks for dropping by, hope you find some of my work interesting.")

    def create_readme(self):
        with open("README.md", "w") as f:
            f.write("# Introduction\n")
            f.write("Hi there! My name is **{}** and I am a **{}**.\n".format(self.name, self.role))
            f.write("I am fluent in the following languages: {}.\n".format(", ".join(self.languages)))
            f.write("# Skills\n")
            f.write("- Python\n")
            f.write("- JavaScript\n")
            f.write("- HTML/CSS\n\n")
            f.write("# Projects\n")
            for project in self.projects:
                f.write("- {}\n".format(project))
            f.write("# Contact\n")
            f.write("Feel free to contact me at [email](mailto:{}) or [LinkedIn](https://www.linkedin.com/in/{}/).\n".format(self.email, self.linkedin))

me = SoftwareEngineer("Zhenye Na", "Software Engineer", ["zh_CN", "en_US"], "email@example.com", "username")
me.add_project("[Project 1](https://github.com/username/project1)")
me.add_project("[Project 2](https://github.com/username/project2)")
me.create_readme()
```
