# 👋 Hi, I'm Tiago!

```js
const getAge = (birthDate) => {
  const today = new Date();
  const birth = new Date(birthDate);
  let age = today.getFullYear() - birth.getFullYear();
  
  // Adjust if birthday hasn't happened yet this year
  const hasBirthdayPassed = 
    today.getMonth() > birth.getMonth() || 
    (today.getMonth() === birth.getMonth() && today.getDate() >= birth.getDate());

  if (!hasBirthdayPassed) {
    age--;
  }

  return age;
};

const Tiago = {
  name: "Tiago",
  birthDate: "1994-06-25",
  age: getAge("1994-06-25"),
  profession: "React and JavaScript Developer",
  passions: ["coding", "technology", "music", "coffee"],
  stack: {
    frontend: ["React", "JavaScript", "HTML", "CSS"],
    backend: ["Node.js", "Express"],
    database: ["MongoDB", "MySQL"],
    tools: ["Git", "VSCode"]
  },
  contact: {
    email: "tiago.abreu.laibacas@example.com",
    linkedin: "https://www.linkedin.com/in/tiago-laibacas/",
  },
  message: () => {
    console.log("Thanks for visiting my profile! 🚀");
  }
}

Tiago.message();
console.log(`Tiago is ${Tiago.age} years old.`);
