## Crucial Framework Documentation

### Framework Functions (Server)
```markdown
local player = exports['crucial']:GetPlayer(source)

player.getDeathStatus() 
player.setDeathStatus(status) --- 0 = elävä 1 = kuollut
player.getPos() 
player.getChar()
player.getJob() -- Return job, rank, duty
player.giveJob(job, value)
player.getIdentifier()
player.getGroup()
player.getPlayerFirstName()
player.getPlayerLastName()
player.getPlayerYear()
player.getPlayerHealth()
player.getPlayerArmor()
player.getPlayerHunger()
player.getPlayerThirst()
player.hasItem(item)
player.hasItemAmount(item, amount)
player.giveGroup(group)

**Currency**
player.getBank() --- Pankkilillä oleva summa
player.getAccountNumber() --- Pankkitilin tilinumero
player.getSecondaryBank() --- Säästötilillä oleva summa
player.getSecondAccountNumber() --- Säästötilin tilinumero
player.giveBank(amount)
player.giveSecondaryBank(amount)
player.removeBank(amount)
player.removeSecondaryBank(amount)

**Items**
player.addItem(name, count) --- Itemit sekä aseet
player.removeItem(name, count)
player.hasItem(name)
player.hasItemAmount(name,, count)
player.weaponAmmo(name, count, val) --- val = true antaa ammuksia, val = false poistaa ammuksia
player.setWeaponAmmo(name, count)
player.getItemLabel(item)
player.getItemType(item) --- Item or weapon
player.getItemWeight(item) --- in grams
player.getItemDurability(item) --- Max durability
player.isItemUsable(item)
player.clearItems()

**Creditscore**
player.getCreditScore()
player.giveCreditScore(amount)
player.removeCreditScore(amount)
```

### Framework Functions (Callbacks)
```markdown
**Client:**
exports['crucial']:TriggerServerCallback('eventName', function() 
    
end)

**Server:**
exports['crucial']:RegisterCallback('eventName', function(source, cb) 
    
end)

exports['crucial']:RegisterItem('item', function(source, item)
    print('Item used')
end)
```

### Framework Library (Client)
```markdown
exports['crucial_lib']:InsertDistNotify(coords, distance, text, exittext) -- Ilmoittaa annetun ilmoituksen alueelle saavuttaessa

exports['crucial_lib']:InsertBlip(name, scale, sprite, color, shortrange, coords)

exports['crucial_lib']:runNotify(msg, color, time) -- Colors: 1 - basic, 2 - error

exports['crucial_lib']:runProgress(msg, time)
```

### Framework Library (Server)
```markdown
exports['crucial_lib']:logToDC(source, user, title, additional, webhooknum, color)
```
