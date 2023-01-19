```Python
#!/usr/bin/python3
class AboutMe:
    def __init__(self, name: str, role: str, languages: list, email: str, linkedin: str):
        self.name = name
        self.role = role
        self.languages = languages
        self.email = email
        self.linkedin = linkedin
        self.projects = []
    
    def add_project(self, project: str):
        self.projects.append(project)

    def create_readme(self):
        with open("README.md", "w") as f:
            f.write("# Introduction\n")
            f.write(f"Hi there! My name is **{self.name}** and I am a **{self.role}**.\n")
            f.write(f"I am fluent in the following languages: {', '.join(self.languages)}.\n")
            f.write("# Skills\n")
            f.write("- Python\n- MongoDB\n- HTML5/CSS3\n- Linux\n- Git\n")
            f.write("# Projects\n")
            for project in self.projects:
                f.write(f"- {project}\n")
            f.write("# Contact\n")
            f.write(f"Feel free to contact me at [email](mailto:{self.email}) or 
            [LinkedIn](https://www.linkedin.com/in/{self.linkedin}/).\n")

me = AboutMe("Usachi Grigore", "IT Technician", ["ro_RO", "it_IT", "ru_RU", "en_US"], "qgrisa@gmail.com", "gregurs")
me.add_project("[Project 1](https://github.com/gregorri/comingsoon)")
me.add_project("[Project 2](https://github.com/gregorri/comingsoon)")
me.create_readme()
```
