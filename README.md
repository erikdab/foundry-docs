# foundry-docs

Foundry VTT Documentation

## New World Guidelines

### Setup Users

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

1. Next enable all mods you want to enable.

Recommended modules:
- Better Rolls for 5e
- D&D Beyond Importer
- Drag Ruler
- libWrapper (needed by Better Rolls for 5e)
- PopOut!
- socketlib (needed by PopOut!)
- Tidy5e Sheet

## Configuration

### System Settings

- Allow Polymorphing: test this
- Initiative Dexterity Tiebreaker: good idea
- Disable Experience Tracking: enable for milestone leveling (DM chooses when to level up)

## Architecture

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

## Configuration

### S3 Media Files Optimization

AWS S3 Media Files Integration (should be AMAZING for people joining from different locations):
https://foundryvtt.com/article/aws-s3/
