```js
class Developer {
  constructor(name, birthDate, profession, passions, stack, contact) {
    this.name = name;
    this.birthDate = new Date(birthDate);
    this.profession = profession;
    this.passions = passions;
    this.stack = stack;
    this.contact = contact;
  }

  // Calculates the age dynamically
  getAge() {
    const today = new Date();
    let age = today.getFullYear() - this.birthDate.getFullYear();
    const hasBirthdayPassed = today.getMonth() > this.birthDate.getMonth() ||
      (today.getMonth() === this.birthDate.getMonth() && today.getDate() >= this.birthDate.getDate());

    if (!hasBirthdayPassed) {
      age--;
    }

    return age;
  }

  // Displays stack skills dynamically
  displayStack() {
    console.log("🛠 My Tech Stack:");
    for (let category in this.stack) {
      console.log(`${category.charAt(0).toUpperCase() + category.slice(1)}:`);
      this.stack[category].forEach(skill => {
        console.log(`- ${skill}`);
      });
    }
  }

  // Displays contact information
  displayContact() {
    console.log("\n📞 Contact Information:");
    Object.entries(this.contact).forEach(([platform, link]) => {
      console.log(`${platform.charAt(0).toUpperCase() + platform.slice(1)}: ${link}`);
    });
  }

  // Greeting message
  greet() {
    console.log(`Hello, my name is ${this.name} and I am a ${this.profession}!`);
    console.log(`Thanks for visiting my profile! 🚀`);
    console.log(`I am ${this.getAge()} years old.`);
  }
}

// Creating an instance of the Developer class
const tiago = new Developer(
  "Tiago",
  "1994-06-25",
  "React and JavaScript Developer",
  ["coding", "technology", "music", "coffee"],
  {
    frontend: ["React", "JavaScript", "HTML", "CSS"],
    backend: ["Node.js", "Express"],
    database: ["MongoDB", "MySQL"],
    tools: ["Git", "VSCode"]
  },
  {
    email: "tiago.abreu.laibacas@example.com",
    linkedin: "https://www.linkedin.com/in/tiago-laibacas/",
    github: "https://github.com/tiago-laibacas"
  }
);

// Calling methods
tiago.greet();
tiago.displayStack();
tiago.displayContact();
