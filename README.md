# adduser

![Coding](https://media.tenor.com/qJ5evVs-_uUAAAAC/coding.gif)

**A Facebook Messenger bot command to add users to a group using their Facebook profile link or numeric user ID.**

Developed by **CodeWithTanim**.

[GitHub Repository](https://github.com/CodeWithTanim/adduser)

## Features

- **Add Users by ID:** Add a user using their numeric Facebook user ID.
- **Add Users by Profile Link:** Accept a Facebook profile URL and attempt to retrieve the user's ID.
- **Automatic User ID Detection:** Extract the user ID and profile name from supported Facebook page responses.
- **Duplicate Member Detection:** Check whether the user is already a member of the group.
- **Group Integration:** Perform the add-user operation in the current Messenger group.
- **Error Handling:** Display an error message when a user cannot be added or their ID cannot be found.
- **Group Approval Awareness:** Check the group's approval mode and provide a corresponding status message.
- **Permission Configuration:** Configure the command for administrator-level use through the bot framework.
- **Command Cooldown:** Configure a five-second cooldown.
- **User Feedback:** Display messages for successful additions, existing members, invalid input, and failures.
- **Lightweight JavaScript Implementation:** Built using an asynchronous Node.js command handler.

## Requirements

- Node.js
- A compatible Facebook Messenger bot framework
- A working bot session with access to the target group
- Appropriate permissions and platform access to add group members
- The framework's supported API methods, including `getThreadInfo()` and `addUserToGroup()`

## Installation

1. Download or clone this repository.

   ```bash
   git clone https://github.com/CodeWithTanim/adduser.git
   ```

2. Open your Messenger bot's command directory.

3. Copy the command file into that directory and name it:

   ```text
   adduser.js
   ```

4. Make sure your bot framework supports the APIs and dependencies used by the script.

5. Restart your Messenger bot.

6. Open a Messenger group where the bot is available and use the command prefix configured in your bot.

## Usage

Use your bot's configured prefix followed by `adduser` and a Facebook user ID or supported Facebook profile link.

### Add a user by ID

```text
<prefix>adduser 123456789012345
```

### Add a user by profile link

```text
<prefix>adduser https://www.facebook.com/username
```

Replace `<prefix>` with your bot's actual command prefix and replace the example ID or profile URL with the intended user's information.

## How It Works

1. The bot receives the `adduser` command in a group conversation.
2. It retrieves the current group's information and member list.
3. It checks whether the provided argument is a numeric ID or a profile link.
4. For a profile link, the script attempts to retrieve the user's ID and name.
5. It checks whether the user is already in the group.
6. If the user is not already a member, it calls the bot framework's `addUserToGroup()` method.
7. The bot sends a status message indicating the result or a failure.

## Command Configuration

| Property | Value |
|---|---|
| Command Name | `adduser` |
| Version | `2.4.3` |
| Author | CodeWithTanim |
| Category | `group` |
| Permission Level | `2` |
| Cooldown | 5 seconds |
| Description | Add a user to a group by link or ID |

Permission levels and command prefixes depend on the bot framework configuration.

## Response Messages

The command can return messages such as:

- `Please enter 1 id/link profile user need to add.`
- `User ID not found.`
- `Member are already in the group.`
- `Can't add user to group.`
- `Added member to group !`
- `Add member to the approved list !`

The actual message depends on the input, group state, and API result.

## Important Notes

- Adding a user may fail because of Facebook restrictions, group settings, privacy settings, or insufficient bot permissions.
- A profile URL does not always provide enough information to resolve a user ID.
- The profile lookup function uses obfuscated code and should be audited before production use.
- The script relies on a bot framework API rather than an official, universally supported Messenger bot interface.
- The group approval workflow should be tested carefully because the script attempts to add the user before checking the approval-mode condition.
- Use the command responsibly and only add people who have agreed to join or where adding them is otherwise appropriate.

## Connect With Me

<p align="left">
  <a href="https://github.com/CodeWithTanim" target="_blank">
    <img align="center" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" alt="GitHub" height="30" width="40" />
  </a>
  <a href="https://x.com/CodeWithTanim" target="_blank">
    <img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/twitter.svg" alt="X (Twitter)" height="30" width="40" />
  </a>
  <a href="https://facebook.com/CodeWithTanim" target="_blank">
    <img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/facebook.svg" alt="Facebook" height="30" width="40" />
  </a>
  <a href="https://instagram.com/CodeWithTanim" target="_blank">
    <img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/instagram.svg" alt="Instagram" height="30" width="40" />
  </a>
  <a href="https://youtube.com/@CodeWithTanim" target="_blank">
    <img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/youtube.svg" alt="YouTube" height="30" width="40" />
  </a>
</p>

Website: [codewithtanim.is-a.dev](http://codewithtanim.is-a.dev)

## Thank You

Thank you for checking out this project!

If you find this command useful, consider starring the repository and sharing your feedback.

**Developed with care by MSRTanim | CodeWithTanim**
