---
title: Dialogue System Framework for Unity (Part 1)
date: 2026-06-16 02:00 +700
categories: [Engine]
tags: [video games, unity, game design]
description: The Dialogue System supporting Unity developer for their narrative design and implementation.
image: assets/img/dialogue/dl-tree.png
---
> Because the article for Dialogue System Framework is so long and to make sure not having the TL;DR issue, this first part will introduce the framework and its structure only.
{: .prompt-info} 

## Introduction 💭
This is a framework I made as the process for my **Graduation Thesis** which is used to support game developer, game writer or game designer to create, manage and implement dialogue to their video game project on **Unity**. This framework can work well with both linear and non-linear storytelling. 

## Structure
The logic for the dialogue contains two crucial parts and one support element:
### Dialogue Node
 This is, in logically, a data storage which contains the all the information of a single speaker's speech, like speaker's name, poitraits, speech's contents, event triggers and branch's ID for next dialogue node. In Unity, ScriptableObject is the most suitable data storage for creating Dialogue Node's logic. 

![Dialogue Node ScriptableObject](/assets/img/dialogue/dl-so-node.png)
_My Dialogue Node structure_

---

### Dialogue
 If Dialogue Node is used to store speakers' speech information, then Dialogue is used to store all the nodes with the connection to each others, to present it in the video game product. Dialogue use **Directed Graph** data structure, so that branching options can be created, connected and directed to each others (for non-linear dialogue system). In Unity, Dialogue is also used ScritableObject for its logic. However, when showing Dialogue in Inspector tab, it is very hard to manage the node since the Inspector presents Dialogue in array.

![Dialogue ScriptableObject](/assets/img/dialogue/dl-so-dialogue.png)
_My Dialogue structure_

---

### The Dialogue Editor
 To solve the problem of the Dialogue management, Dialogue Editor is created. This is a custom editor which is programmed using **UnityEditor**, a namespace contain essential components to create a custom editor window for Unity by your own ideas. My editor, like its name, created to easily manage the structure of a Dialogue, like adding, linking and deleting nodes. Or easily adjust the content of a single Dialogue Node by click on the desired one. 

![Dialogue Editor](/assets/img/dialogue/dl-editor.png)
_A Dialogue within The Dialogue Editor_ 

The next part will show the way the Dialogue is presented on a Unity project's Scene. Right now, below is the Github link to the repository containing the source for my framework.

[![Static Badge](https://img.shields.io/badge/GitHub-%23181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/vntortoise724/Unity-Dialogue-Framework)

Hope to see you at the next part 👋

---

#### Many Thanks - Xin Cảm Ơn -吀感恩
