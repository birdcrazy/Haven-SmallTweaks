# Haven-SmallTweaks
A collection of custom css mods to tweak the [ancsemi/Haven](https://github.com/ancsemi/Haven) web-app layout.

## The Tweaks
### Big-Tweak
Contains all of the smallTweaks combined in one file

### chat-bubbles
Adds backround bubbles to messages to make each message appear more distinct.

<details>

<summary>Photos</summary>

| Client     | Original     | Tweaked |
| ----------- | ----------- | ----------- |
| Desktop | <img width="496" height="223" alt="image" src="https://github.com/user-attachments/assets/70805e5c-c044-4690-8d80-b855abbed441" /> |  <img width="504" height="225" alt="image" src="https://github.com/user-attachments/assets/2d684aaf-77cf-4c47-ac2e-9c0a4b93a73a" /> |
| Mobile | <img width="434" height="312" alt="image" src="https://github.com/user-attachments/assets/b9c253e8-14c1-4650-b147-993a4ce6730b" /> | <img width="439" height="291" alt="image" src="https://github.com/user-attachments/assets/910ba49b-48e5-4ccf-8815-cfa7a82d015b" />  |

</details>


### compact-create-options
Makes channel creation options more compact to use less virtical space in the sidebar. 

This provides a little more room for the channel list when create-channel section is expanded

<details>

<summary>Photos</summary>

| Original     | Tweaked |
| ----------- | ----------- |
| <img width="262" height="311" alt="image" src="https://github.com/user-attachments/assets/c479558f-38d5-4dd6-9ff8-4d6481338e6a" /> |  <img width="263" height="266" alt="image" src="https://github.com/user-attachments/assets/317d3167-d619-4364-a61a-6fb51a460681" /> |

</details>

### full-scroll-dock
Changes the multiple channel scroll areas to one single scroll area. 

This Provides easier channel/DM navigation on small screens and/or when there are a lot of channels and DMs.

<details>

<summary>Photos</summary>

| Original     | Tweaked |
| ----------- | ----------- |
| <img width="265" height="635" alt="image" src="https://github.com/user-attachments/assets/91d1b6a3-ba6a-4d2c-94a1-ef0b7d7e6173" /> |  <img width="269" height="640" alt="image" src="https://github.com/user-attachments/assets/a059d1e8-e802-4a53-b228-e03654e02b1f" /> |

</details>

### left-message-toolbar
Moves the message toolbar to the left side of messages _(Only effects desktop/large-screens)_

Sometimes I find it dificult on wide screens to drag the mouse all the way to the right of the message to open the message toolbar for the correct message.

This tweak makes it easier to ensure I am using the toolbar for the intended message.

<details>

<summary>Photos</summary>

| Original     | Tweaked |
| ----------- | ----------- |
| <img width="598" height="232" alt="image" src="https://github.com/user-attachments/assets/2ff50156-9ecd-4d71-9ab5-d37a06b517ae" /> |  <img width="605" height="254" alt="image" src="https://github.com/user-attachments/assets/571d8a8e-a4cf-4624-99cd-c49e22e39f09" /> |

</details>

### left-settings-button
When on desktop or large screen: Moves the settings button to the left dock and removes the settings button from the right-dock/user-list

Gives more room to see users in the user list

_(this is already done by default on mobile and small screens, this tweak just impliments it on large screens also)_

<details>

<summary>Photos</summary>

| Original     | Tweaked |
| ----------- | ----------- |
| <img width="896" height="109" alt="image" src="https://github.com/user-attachments/assets/d5cb3005-711b-4165-aad0-9a1750108f81" /> | <img width="892" height="109" alt="image" src="https://github.com/user-attachments/assets/839d0941-69a5-4a86-88ee-79371f731b55" />  |

</details>

### mobile-sidebars-extended
Reduces wasted space in the left and right sidebars to provide more viewable area for content

_(Only takes effect on mobile and small screens)_

<details>

<summary>Photos</summary>

| Dock     | Original     | Tweaked |
| ----------- | ----------- | ----------- |
| Left  | <img width="295" height="119" alt="image" src="https://github.com/user-attachments/assets/caddea20-11db-4faa-91e5-bf6e2789a277" /> |  <img width="293" height="114" alt="image" src="https://github.com/user-attachments/assets/896ab4a0-f992-4f17-9bb1-d451d4661656" /> |
| Right | <img width="267" height="478" alt="image" src="https://github.com/user-attachments/assets/1267a67f-5d5d-416b-80d3-cf13c0f2345e" /> | <img width="263" height="479" alt="image" src="https://github.com/user-attachments/assets/d2f8d8e7-d3e5-495f-98b1-9c90fed8321d" />  |

</details>

### top-voice-settings
Moves the voice settings up, to be closer the voice users; Rather than at the bottom of the dock, where it seems a little disassociated with the voice-users location.

I always find myself looking at the voice users area, and have trouble finding the voice settings because they are all the way at the bottom of the screen. This tweak solves this issue for me.

<details>

<summary>Photos</summary>

| Original     | Tweaked |
| ----------- | ----------- |
| <img width="260" height="548" alt="image" src="https://github.com/user-attachments/assets/3051cb2a-a950-45d2-b87d-8317d541dffc" /> | <img width="259" height="550" alt="image" src="https://github.com/user-attachments/assets/dd431092-a462-45b8-b25a-580f3fd2b3a2" /> |

</details>


## Installation
### Bash Script
Run the following script on the host. (Replace "haven" in the script with your haven container name.)

```
git clone --depth 1 --filter=blob:none --sparse https://github.com/birdcrazy/Haven-SmallTweaks.git /tmp/smalltweaks-repo && \
cd /tmp/smalltweaks-repo && \
git sparse-checkout set themes && \
tar -C themes -cf - . | docker exec -i haven tar -C /app/themes -xf - && \
cd .. && \
rm -rf /tmp/smalltweaks-repo
```

### Manual
Download the repo, move the contents of `/themes` to your haven server's `/app/themes` folder


## Usage
In Haven, go to user settings / Plugins & Themes. Then enable the tweaks to your preference

The tweaks are modular; They can be applied indipendantly, or together.
