# 🛡️ WatchTower Security Bot - User Guide

![Discord.js](https://img.shields.io/badge/Discord.js-v14-7289DA?style=for-the-badge&logo=discord&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-v18+-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-4.4+-47A248?style=for-the-badge&logo=mongodb&logoColor=white)

> **Last Updated:** August 24, 2025  
> **Developer:** [@demondev_](https://discord.com/users/demondev_)  
> **GitHub:** [@demondevx](https://github.com/demondevx)  
> **Support Server:** [Join Here](https://discord.gg/D2hrnpjZuC)

---

## 🚀 **Getting Started**

### **Adding WatchTower to Your Server**
1. Click the invite link [here](https://discord.com/oauth2/authorize?client_id=1408972596187496509&permissions=8&integration_type=0&scope=bot+applications.commands)
2. Select your server from the dropdown
3. Grant the necessary permissions
4. Click "Authorize"

### **Required Permissions**
- **Administrator** (Recommended for full functionality)
- **Manage Roles** (For verification system)
- **Manage Channels** (For anti-nuke protection)
- **Ban Members** (For moderation commands)
- **Kick Members** (For moderation commands)

---

## 🛡️ **Core Features**

### **Anti-Nuke Protection**
WatchTower provides comprehensive protection against server nuking with **20+ protection types**:

#### **Instant Protections** (No limits, immediate action)
- **Anti Ban** - Prevents unauthorized bans
- **Anti Kick** - Prevents unauthorized kicks
- **Anti Channel Delete** - Prevents channel deletion
- **Anti Role Delete** - Prevents role deletion
- **Anti Emoji Delete** - Prevents emoji deletion
- **Anti Emoji Rename** - Prevents emoji renaming
- **Anti Invite Delete** - Prevents invite deletion
- **Anti Server Icon** - Prevents icon changes
- **Anti Server Rename** - Prevents server renaming
- **Anti Vanity Change** - Prevents vanity URL changes

#### **Protections with Limits** (Configurable action limits)
- **Anti Role Create** - Limits role creation
- **Anti Channel Create** - Limits channel creation
- **Anti Role Rename** - Limits role renaming
- **Anti Channel Rename** - Limits channel renaming
- **Anti Role Permission Update** - Limits permission changes
- **Anti Dangerous Role Add** - Limits dangerous role assignments
- **Anti Bot Add** - Limits bot additions
- **Anti Prune** - Limits member pruning
- **Anti Mention** - Limits mass mentions

---

## 📋 **Command Reference**

### **🛡️ Security Commands**

#### **`/anti-nuke`** - Main anti-nuke management
- **`status`** - View all protection statuses
- **`enable`** - Enable anti-nuke system
- **`disable`** - Disable anti-nuke system
- **`config`** - Configure protection settings
- **`enable-protection <type>`** - Enable specific protection
- **`disable-protection <type>`** - Disable specific protection

#### **`/anti-raid`** - Anti-raid protection
- **`status`** - View anti-raid status
- **`enable`** - Enable anti-raid protection
- **`disable`** - Disable anti-raid protection

#### **`/whitelist`** - Manage whitelisted users
- **`add-user <user> <reason>`** - Add user to whitelist
- **`remove-user <user>`** - Remove user from whitelist
- **`list`** - View all whitelisted users

#### **`/factory-reset`** - Reset all bot settings to default

### **🛠️ Moderation Commands**

#### **`/moderation`** - Main moderation hub
- **`ban <user> <reason>`** - Ban a user
- **`kick <user> <reason>`** - Kick a user
- **`mute <user> <duration> <reason>`** - Mute a user
- **`unmute <user>`** - Unmute a user
- **`warn <user> <reason>`** - Warn a user
- **`clear <amount>`** - Clear messages
- **`unban <userid>`** - Unban a user

### **✅ Verification Commands**

#### **`/verification`** - Verification system management
- **`setup <channel>`** - Set up verification channel
- **`disable`** - Disable verification system

### **📝 Logging Commands**

#### **`/logging`** - Manage logging settings
- **`setup <channel>`** - Set up logging channel
- **`disable`** - Disable logging

### **⚙️ Setup Commands**

#### **`/setup`** - Server setup and configuration
- **`scan`** - Scan server for security issues
- **`backup`** - Create server backups

#### **`/config`** - View server configuration

### **📚 General Commands**

#### **`/help`** - View help menu and command categories
#### **`/guide`** - Detailed guides for bot features
#### **`/botinfo`** - View bot statistics and information

---

## 🔧 **Configuration Guide**

### **Setting Up Anti-Nuke Protection**

1. **Enable the system:**
   ```
   /anti-nuke enable
   ```

2. **Configure specific protections:**
   ```
   /anti-nuke enable-protection ban
   /anti-nuke enable-protection channelDelete
   /anti-nuke enable-protection roleDelete
   ```

3. **Set action limits (for protections with limits):**
   ```
   /anti-nuke config ban punishment:kick limit:5 
   ```

### **Setting Up Verification System**

1. **Create verification channel:**
   ```
   /verification set-channel #verification
   /verification set-role @verified
   ```

2. **The bot will automatically:**
   - Create an "Unverified" role
   - Set up channel permissions
   - Post verification panel
   - Configure auto-role assignment

### **Setting Up Logging**

1. **Create logging channel:**
   ```
   /logging set #logs
   ```

2. **The bot will log:**
   - Moderation actions
   - Anti-nuke events
   - Server changes
   - Security violations

---

## 🚨 **Understanding Punishments**

### **Punishment Types**
- **Ban** - Permanently removes user from server
- **Kick** - Removes user from server (can rejoin)
- **Role Removal** - Removes specific roles

### **Action Limits**
- **Protections with limits** allow a certain number of actions before punishment
- **Instant protections** trigger immediately on violation
- **Configurable limits** can be set per protection type

---

## 🛡️ **Security Best Practices**

### **Recommended Settings**
1. **Enable all instant protections** for maximum security
2. **Set reasonable limits** for protections with limits
3. **Use whitelist** for trusted administrators
4. **Monitor logs regularly** for suspicious activity
5. **Keep bot permissions** at Administrator level

### **Whitelist Management**
- **Add server owners** to whitelist automatically
- **Add trusted moderators** who need to perform administrative actions
- **Regularly review** whitelist for unnecessary entries

---

## 🔍 **Troubleshooting**

### **Common Issues**

#### **Bot not responding to commands**
- Check if bot has proper permissions
- Verify bot is online and in your server
- Ensure commands are properly registered

#### **Anti-nuke not working**
- Verify bot has Administrator permissions
- Check if specific protections are enabled
- Review whitelist for exempt users

#### **Verification system issues**
- Ensure bot can manage roles
- Check channel permissions
- Verify "Unverified" role exists

### **Getting Help**
- **Support Server:** [Join Here](https://discord.gg/D2hrnpjZuC)
- **GitHub Issues:** [Report Bugs](https://github.com/demondevx)
- **Developer Contact:** [@demondev_](https://discord.com/users/demondev_)

---

## 📊 **Bot Statistics**

- **Commands:** 13+ slash commands
- **Protections:** 20+ anti-nuke protections
- **Events:** Real-time security monitoring
- **Database:** MongoDB for persistent storage
- **Uptime:** 99.9% reliability

---

## 🔗 **Useful Links**

- **Support Server:** [https://discord.gg/D2hrnpjZuC](https://discord.gg/D2hrnpjZuC)
- **Developer Discord:** [@demondev_](https://discord.com/users/demondev_)
- **GitHub Profile:** [@demondevx](https://github.com/demondevx)
- **Bot Invite:** [Add to Server](https://discord.com/oauth2/authorize?client_id=1408972596187496509&permissions=8&integration_type=0&scope=applications.commands+bot)

---

## 📝 **Changelog**

### **Version 1.0.0** - August 24, 2025
- Initial release
- 20+ anti-nuke protections
- Comprehensive moderation tools
- Verification system
- Advanced logging
- Anti-raid protection

---

*For the latest updates and support, join our [Support Server](https://discord.gg/D2hrnpjZuC)!*

---

**© 2025 WatchTower Security Bot. Developed by [@demondevx](https://github.com/demondevx)**
