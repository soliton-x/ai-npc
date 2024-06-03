<div align="center">

# NPC Playground 🕹️🤖

[![Discord][discord-badge]][discord]

3D playground to interact with LLM-powered NPCs. </br>
Modify the `world.lua` file to teach them new skills with a few lines of code.

<img width="1342" alt="cubzh_gigax_hf" src="https://github.com/soliton-x/ai-npc/assets/33256624/e62dd138-c018-4ecf-bc77-a072fadb5c12">

[Installation](#Installation)
[Customization](#Customization)
[Course](#Course)
[Credits](#Credits)

</div>


## Installation

1. Fork the project on [Hugging Face](https://huggingface.co/projects/ai-npc-world).
2. Modify the [`world.lua`](https://huggingface.co/spaces/cubzh/ai-npcs/blob/main/world.lua) file to edit NPC skills!
3. Deploy on your own Hugging Face space to run your modified version of the playground.


## Customization

### **Tweaking NPC Behavior**
Modify the fields defined in `world.lua`'s `NPCs` table in order to influence NPC behaviour:
```lua
local NPCs = {    
  {
    name = "npcscientist",
    physicalDescription = "A small sphere with a computer screen for a face",
    psychologicalProfile = "Designed to be helpful to any human it interacts with, this robot viscerally hates squirrels.",
    currentLocationName = "Scientist Island",
    initialReflections = {
      "This NPC is a robot that punctuates all of its answers with electronic noises - as any android would!",
      ...
    },
  },
  ...
}
```
 
### **Teaching NPCs new skills** 
Our NPCs have been trained to use any skill you've defined before running the game. This is achieved by training the LLM powering them to do "function calling". 

Modify `world.lua`'s `skills` table to give your NPCs new skills :
```lua
local skills = {
	{
    name = "SAY",
    description = "Say smthg out loud",
    parameter_types = {"character", "content"},
    callback = function(client, action)
      local npc = client:getNpc(action.character_id)
      if not npc then print("Can't find npc") return end
        dialog:create(action.content, npc.avatar)
      print(string.format("%s: %s", npc.name, action.content))
    end,
    action_format_str = "{protagonist_name} said '{content}' to {target_name}"
  },
  ...
}
```
The `callback` will be called whenever an NPC uses this skill, using the parameters defined in the `parameters` field. We've given you some examples in `skills.lua`, feel free to draw inspiration from them!  

### [Work in progress] **Environment Design:** 
The Cubzh game engine allows you to modify the 3D environment of your worlds, by importing community-generated voxel assets or creating new ones yourself. We're working hard to integrate these functionalities into this world - stay tuned!

## Course

Together with the HuggingFace staff, we've released a new course to teach you how to create your own Lua skills. 
You can access it [here](https://huggingface.co/huggingface-ml-4-games-course)

## Credits

- [Hugging Face](https://huggingface.co/) 🤗
- [Gigax](https://github.com/GigaxGames)
- [Cubzh](https://cu.bzh): A versatile UGC (User-Generated Content) gaming platform.
- **You !** You're welcome to fork the repo, share your creations, and create PRs here :)


---

For detailed documentation, troubleshooting, and contributing guidelines, please refer to the [wiki](https://github.com/Cubzh/ai-npc-world/wiki).

[discord]: https://discord.gg/rRBSueTKXg
[discord-badge]: https://img.shields.io/discord/1090190447906934825?color=81A1C1&logo=discord&logoColor=white&style=flat-square
