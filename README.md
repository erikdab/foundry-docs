# foundry-docs

Foundry VTT Documentation

## Player Guide

Tutorial (start here): https://foundryvtt.com/article/player-orientation/

General:
- Knowledge Base: https://foundryvtt.com/kb/
- Controls: https://foundryvtt.com/article/controls/
- Game Settings: https://foundryvtt.com/article/settings/

Drawing: https://foundryvtt.com/article/drawings/

Tokens: https://foundryvtt.com/article/tokens/

Measurement and Templates: https://foundryvtt.com/article/measurement/

Dice:
- Simple Dice: https://foundryvtt.com/article/dice/
- Advanced Dices: https://foundryvtt.com/article/dice-advanced/
- Dice Modifiers: https://foundryvtt.com/article/dice-modifiers/

## Gamemaster Guide

Tutorial: https://foundryvtt.com/article/tutorial/

Foundry VTT Tutorial video series: https://www.youtube.com/watch?v=-aHlApa1nUA

Knowledge Base: https://foundryvtt.com/kb/

Creating Game Worlds:
- Documentation: https://foundryvtt.com/article/game-worlds/
- Personal [Game World Guidelines](#game-world-guidelines)

Map Notes: https://foundryvtt.com/article/map-notes/

Walls: https://foundryvtt.com/article/walls/

Tiles: https://foundryvtt.com/article/tiles/

Sounds: https://foundryvtt.com/article/ambient-sound/

Canvas Layers: https://foundryvtt.com/article/canvas-layers/

Lighting: https://foundryvtt.com/article/lighting/

## Game World Guidelines

### Setup Users

[Documentation](https://foundryvtt.com/article/users/)

Open User Management:

1. Go to Game Settings
2. Go to User Management

Change Gamemaster password:

1. Enter a different password for Gamemaster user
2. Click Save and Return

Configure Permissions (change what each user type can do):

1. Click Configure Permissions
2. Configure user roles using the checkpoint

### Modules (Plugins)

1. Go to Game Settings
2. Click on Manage Modules
3. Use the checkboxes to enable desired modules

Recommended modules:
- Better Rolls for 5e
- D&D Beyond Importer
- Drag Ruler
- libWrapper (needed by Better Rolls for 5e)
- PopOut!
- socketlib (needed by PopOut!)
- Tidy5e Sheet

Premium Content:
- Prepared! (some premade adventures)

Potential modules:
- https://foundryvtt.com/packages/My-Shared-Compendia

## World Configuration

### System Settings

- Allow Polymorphing: test this
- Initiative Dexterity Tiebreaker: good idea
- Disable Experience Tracking: enable for milestone leveling (DM chooses when to level up)

### Module Settings

#### Drag Ruler

- Show GM ruler to players: disable maybe? To allow GM to measure distances anytime

## System Configuration

Installation documentation: https://foundryvtt.wiki/en/setup/linux-installation

Parts:
- [FoundryVTT](https://foundryvtt.com) server running on Linux/NodeJS
- [duckdns.org](https://www.duckdns.org) for dynamic dns (can use router to update)
- [Caddy](https://caddyserver.com/docs/automatic-https) for HTTPS encryption
- [PM2](https://pm2.keymetrics.io/docs/usage/quick-start/) for process management: 

### Dynamic DNS Router configuration

Router DDNS configuration (DuckDNS):
* the hostname is the prefix to your domain (e.g., loganmarchione.duckdns.org)
* the username is nouser (don’t use your account name)
* the password is your account token (that long string of numbers/letters)

Cool idea if I want my own DDNS setup: https://github.com/awslabs/route53-dynamic-dns-with-lambda
### Port forwarding

- Use separate VLAN for security to limit blast radius
- Disable UPnP in Foundry VTT and configure port forwarding manually
- Port forward only HTTPS

## Future Considerations

- Automatically shutdown machine and turn on when users are trying to connect to it?
- Investigate raspberry pi performance

### S3 Media Files Optimization

AWS S3 Media Files Integration (should be AMAZING for people joining from different locations):
https://foundryvtt.com/article/aws-s3/

### Backup

- Plan to upgrade to S3 together with lifecycle policy to delete old backups
- Script to backup with cron, script to restore from backup