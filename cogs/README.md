# Cogs

## Summary

All extensions, also known as cogs, are contained within this folder. The cogs can be dynamically loaded and unloaded at runtime, which allows for the removal or addition of features without requiring the entire bot to be restarted. The `/cogs` command in `system.py` is responsible for handling this process.

## Must be met

1. All cogs must inherit from [class Base](base.py).
2. Cog's file name must be same as class name. File name is lowercase, class name is CamelCase.
3. If there is task in cog it must be initialized in `self.tasks` list.
4. Comment at the beginning of the file summarizing function of cog.
5. All cogs should be included in cogs folder and added to the README.

## List of Cogs

### [Absolvent](absolvent.py)

Cog for diploma verification. When successful, the user is given role Survivor(Bc.) or King(Ing.).\
**Commands:**

    - /diplom help
    - /diplom
---

### [AutoPin](autopin.py)

Cog controlling auto pinning of messages and priority pins in channels.\
**Commands:**

    - ?pin
    - ?pin add
    - ?pin remove
    - ?pin list
---

### [Bookmark](bookmark.py)

Cog controlling bookmarks. The bot will send copy of message to user.\
**Commands:**

    - react 🔖
    - message_command "Bookmark"
---

### [DynamicConfig](dynamicconfig.py)

Cog for dynamicaly changing config.\
**Commands:**

    - ?config
    - ?config set
    - ?config append
    - ?config load
    - ?config list
    - ?config get
    - ?config backup
    - ?coonfig sync_template
---

### [Error](error.py)

Cog for handling command errors. This is mostly for logging purposes.
Errors originating from other then commands (such as reaction handlers and listeners) are handled in rubbergod.py `on_error` function.

---

### [Exams](exams.py)

Cog to parse exams data from website and send it to channel.
Available for each year of study.\
**Commands:**

    - /terms
    - /terms update
    - /terms remove_all
    - /terms remove
    - /terms start
    - /terms stop
    - /exams

**Tasks:**

    - update_terms_task
---

### [FitRoom](fitroom.py)

Cog for finding rooms on FIT BUT.\
**Commands:**

    - /room
---

### [FitWide](fitwide.py)

Cog implementing management of year roles and database of user logins.\
**Commands:**

    - ?role_check
    - ?increment_roles
    - ?update_db
    - ?get_db
    - ?get_user_login
    - ?get_login_user
    - ?reset_login
    - ?connect_login_to_user
---

### [Fun](fun.py)

Cog containing commands that call random APIs for fun things.\
**Commands:**

    - /cat
    - /dog
    - /fox
    - /duck
    - /dadjoke
    - /yo_mamajoke
---

### [GrillbotApi](grillbotapi.py)

Functions and commands that communicate with the Grillbot API.

---

### [Help](help.py)

Cog containing help command. Only shows commands that user has access to
and are context commands.\
**Commands:**

    - ?help
---

### [Hugs](hugs.py)

Cog implementing hug commands. Send hug to user and see leaderboard.\
**Commands:**

    - /hug hugboard
    - /hug huggersboard
    - /hug mosthugged
    - /hug me
    - /hug give
---

### [Icons](icons.py)

Cog implementing dynamic icon system. Users can assign themselves icons from a list of roles.\
**Commands:**

    - /icon
---

### [Info](info.py)

Cog containing commands that get basic information from other sources.\
**Commands:**

    - /urban
    - /pocasi
---

### [IOS](ios.py)

Cog for the IOS subject. Get users on merlin/eva server which have blocking processes running.\
**Commands:**

    - ?ios
    - ?ios_start
    - ?ios_stop
    - ?ios_cancel
**Tasks:**

    - ios_body
---

### [Karma](karma.py)

Cog implementing karma system. Users can give each other positive/negative karma points with reactions.\
**Commands:**

    - /karma me
    - /karma stalk
    - /karma getall
    - /karma get
    - /karma message
    - /karma leaderboard
    - /karma bajkarboard
    - /karma givingboard
    - /karma ishaboard
    - /karma_mod revote
    - /karma_mod vote
    - /karma_mod give
    - /karma_mod transfer
    - user_command Karma uživatele
    - message_command Karma zprávy
---

### [Latex](latex.py)

Cog for interpreting latex commands as images.\
**Commands:**

    - ?latex
---

### [Meme](meme.py)

Cog for meme commands.\
**Commands:**

    - /uhoh
    - ???
    - /bonk
---

### [MemeRepost](memerepost.py)

Cog for handling memes with X number of reactions to be reposted to a specific channel.

---

### [Moderation](moderation.py)

Cog implementing functions for server moderation and help functions for mods.
Implemented logging for tagging @mods.

---

### [Nameday](nameday.py)

Cog for sending name days and birthdays.\
**Commands:**

    - /svatek
    - /meniny
**Tasks:**

    - send_names

---

### [Pet](pet.py)

Cog for petting people.\
**Commands:**

    - /pet

---

### [Random](random.py)

Implementing commands using random module.\
**Commands:**

    - /pick
    - /flip
    - /roll

---

### [Reactions](reactions.py)

Cog for handling reactions and delegating to specific cog.

---

### [Review](review.py)

Cog implementing review system for subjects.\
**Commands:**

    - /review get
    - /review add
    - /review remove
    - /subject update
    - /wtf
    - /tierboard
---

### [Roles](roles.py)

Cog implementing channels and roles management. Copying/creating channels with permissions.\
**Commands:**

    - /do_da_thing
    - /group add
    - /group get
    - /group delete
    - /group list
    - /group add_channel_id
    - /group add_role_id
    - /group reset_channels
    - /group reset_roles
    - /channel copy
    - /channel clone
    - /channel create
---

### [StreamLinks](streamlinks.py)

Cog implementing streamlinks system. List streams for a subject.\
**Commands:**

    - /streamlinks get
    - /streamlinks list
    - /streamlinks_mod add
    - /streamlinks_mod remove
---

### [Studijni](studijni.py)

Cog implementing information about office hours of the study department.\
**Commands:**

    - /studijni
---

### [Subscriptions](subscriptions.py)

Cog implementing subscription to allowed channels. Subscribed users will receive notifications about new messages if they are offline.\
**Commands:**

    - /subscription subscribe
    - /subscription unsubscribe
    - /subscription list
    - /subscription channel
    - /subscription user
---

### [System](system.py)

Core cog for bot. Can't be unloaded. Contains commands for cog management.\
**Commands:**

    - ?git pull
    - /cogs
    - /uptime
---

### [Timeout](timeout.py)

Containing timeout commands and manipulating with timeout.\
**Commands:**

    - /timeout user
    - /timeout remove
    - /timeout list
**Tasks:**

    - refresh_timeout
---

### [Verify](verify.py)

Cog for verification system. Allows users to verify themselves with xlogin00 and gain access to server.\
**Commands:**

    - /verify
    - /dynamic_verify create
    - /dynamic_verify edit
    - user_command Verify host
---

### [Vote](vote.py)

Cog implementing vote and polls feature.\
**Commands:**

    - ?vote
    - ?singlevote
---

### [Warden](warden.py)

Cog for repost detection.\
**Commands:**

    - ?scan
    - ?scan history
    - ?scan message
---

### [Week](week.py)

Cog containing information about week (odd/even) and its relation to calendar/academic week.
**Commands:**

    - /week