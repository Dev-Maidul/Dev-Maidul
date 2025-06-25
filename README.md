<h1 align="center">Hi there 👋, I'm Md Maidul Islam</h1>
<p align="center">
  🌍 Full-Stack Developer | 🎓 CSE Student in Beijing | 🕌 Muslim | 🇧🇩 From Bangladesh
</p>

---

<p align="center">
  <img src="https://github.com/Dev-Maidul/Dev-Maidul/blob/main/github-banner.png">
</p>

```js
### 💫 About Me:

I am a passionate Bangladeshi developer based in Beijing 🇨🇳, currently pursuing a CSE degree. I specialize in building modern full-stack web applications with a strong emphasis on clean code, collaboration, and creating impactful solutions. I'm always excited to connect with new people in the tech community, so feel free to say hi!

const devMaidul = {
  name: "Md Maidul Islam",
  pronouns: "He | Him",
  position: "Full-Stack Web Developer | CSE Student",
  location: "Beijing, China",
  from: "Bangladesh",
  education: {
    degree: "BSc in Computer Science",
    university: "China University of Petroleum"
  },
  skills: {
    frontend: ["HTML", "CSS", "Tailwind CSS", "JavaScript (ES6)", "React.js"],
    backend: ["Node.js", "Express.js"],
    database: ["MongoDB"],
    auth: ["Firebase Authentication"]
  },
  experience: [
    "Teaching Assistant for C Programming (1+ year)",
    "Built 10+ real-world web projects"
  ],
  languages: ["Bengali", "English", "Chinese (basic)"],
  currentFocus: "To contribute to impactful products and secure a remote developer role before December 25."
};

function introduceDeveloper(dev) {
  console.log(`👋 Hi, I'm ${dev.name}, a ${dev.position.split(" | ")[0]} from ${dev.from}, currently based in ${dev.location}.`);
  console.log("🔭 I'm currently focused on:", dev.currentFocus);
  console.log("💻 Tech Stack:");
  console.log("Frontend:", dev.skills.frontend.join(", "));
  console.log("Backend:", dev.skills.backend.join(", "));
  console.log("Database:", dev.skills.database.join(", "));
  console.log("Auth:", dev.skills.auth.join(", "));
  console.log("🌐 Languages I speak:", dev.languages.join(", "));
  console.log("📘 Experience Highlights:");
  dev.experience.forEach((item) => console.log("•", item));
  console.log("📫 Let's connect on GitHub!");
}

introduceDeveloper(devMaidul);
