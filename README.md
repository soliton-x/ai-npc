# AI NPC World 🌍🎮🤖

[Live Demo](https://cu.bzh/demo)

[Join our community Discord: AI NPC Devs](https://discord.gg/xyz123)

<img width="1454" alt="AI NPC World Screenshot" src="https://cu.bzh/assets/npc-world.png">

AI NPC World is a groundbreaking virtual environment where AI NPCs (Non-Player Characters) autonomously interact, adapt, and evolve based on player inputs.

This project is a collaboration between:
- [Hugging Face](https://huggingface.co/): Pioneers in machine learning tools and resources.
- [Gigax](https://github.com/GigaxGames): Innovators in AI models for gaming.
- [Cubzh](https://cu.bzh): A versatile UGC (User-Generated Content) gaming platform.

## Overview

- 💻 [Stack](#stack)
- 🧠 [Installation](#installation)
- 🎨 [Customization](#customization)
- 🚀 [Deployment](#deployment)
- 🏆 [Credits](#credits)

## Stack

- Game Engine: [Cubzh](https://cu.bzh)
- AI Models: [Hugging Face](https://huggingface.co/)
- NPC Behavior Framework: [Gigax](https://github.com/GigaxGames)
- Scripting: Lua
- Frontend: Browser-based 3D simulation

## Features

- **Auto-updating AI Behaviors:** NPCs adapt to player interactions dynamically.
- **Interactive Storytelling:** Players can influence the NPCs and the narrative.
- **Customizable Parameters:** Modify every aspect of NPC behavior and environment.
- **Fork & Hack:** Easily fork the project on Hugging Face to create your own worlds.
- **Voxel Library:** Access a library of 25k voxel items to enhance your game scenes.

## Installation

**Note**: There is a one-click install option for this project on [Hugging Face](https://huggingface.co/projects/ai-npc-world) for those who want to run it without modification.

### 1. Clone the repository and install packages

```bash
git clone https://github.com/Cubzh/ai-npc-world.git
cd ai-npc-world
npm install
```

### 2. Set up Cubzh

Download and install Cubzh following the instructions on their [website](https://cu.bzh).

### 3. Configure the environment

Create a `.env` file in the root directory and add the necessary environment variables:

```env
HUGGING_FACE_API_KEY=your_huggingface_api_key
GIGAX_API_KEY=your_gigax_api_key
```

### 4. Run the simulation

```bash
npm run start
```

You can now access the simulation at http://localhost:3000.

## Customization

1. **NPC Behavior:** Modify NPC scripts in the `scripts/npc/` directory to change their behavior and skills. Some commented lines in the code can enable new skills.

2. **Environment Design:** Use the voxel library to design unique environments. Add or remove items to fit your game's theme.

3. **Story & Dialogue:** Customize NPC dialogues and storylines by editing the Lua scripts in the `scripts/story/` directory.

4. **Fork & Experiment:** Fork the project on Hugging Face to create your own version of AI NPC World and experiment with different AI models and configurations.

## Deployment

### Deploy to your own server

To deploy the project, follow these steps:

1. **Build the project:**

```bash
npm run build
```

2. **Deploy to a server of your choice.** Use platforms like Vercel, Netlify, or any other hosting service to deploy your built project.

### Fork & Deploy on Hugging Face

1. Fork the project on [Hugging Face](https://huggingface.co/projects/ai-npc-world).
2. Customize the project to suit your needs.
3. Use the Hugging Face deployment tools to launch your own version.

## Credits

- **Hugging Face** for providing powerful machine learning models and tools.
- **Gigax** for their advanced AI models tailored for gaming.
- **Cubzh** for the incredible UGC gaming platform and voxel library.
- **Community Contributors** who helped shape and improve the project.

Join us in revolutionizing the gaming world with AI-powered NPCs. Happy gaming!

---

For detailed documentation, troubleshooting, and contributing guidelines, please refer to the [wiki](https://github.com/Cubzh/ai-npc-world/wiki).
