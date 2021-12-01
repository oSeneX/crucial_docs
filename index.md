## Crucial Framework Documentation

### Framework Functions (Client)
```markdown
-
```

### Framework Functions (Server)
```markdown
local player = exports['cc_base']:GetPlayer(source)
player.getdeathStatus() 
player.getPos() 
player.getChar() -- Valittu hahmo (1 & 2)
player.getJob() 
player.giveJob()
player.getDuty()
player.getIdentifier()
player.getGroup()
player.getBank() -- Pankkilillä oleva summa
player.getAccountNumber() -- Pankkitilin tilinumero
player.getSecondaryBank() -- Säästötilillä oleva summa
player.getSecondAccountNumber() -- Säästötilin tilinumero
player.setdeathStatus(status) -- 0 = elävä 1 = kuollut
player.giveGroup(group)
player.giveBank(amount)
player.giveSecondaryBank(amount)

**Items**
player.addItem(name, count) -- Itemit sekä aseet
player.removeItem(name, count)
player.weaponAmmo(name, count, val) -- val = true antaa ammuksia, val = false poistaa ammuksia
player.getItemLabel(item)
player.getItemType(item) -- Item or weapon
player.getItemWeight(item) -- in grams
player.getItemDurability(item) -- Max durability
player.isItemUsable(item)
```

### Framework Functions (Callbacks)
```markdown
**Client:**
exports['cc_base']:TriggerServerCallback('eventName', function() 

end)

**Server:**
exports['cc_base']:RegisterCallback('eventName', function(source, cb) 

end)
```

### Framework Modules (Client)
```markdown
exports['cc_modules']:InsertDistNotify(coords, distance, notifyteksi) -- Ilmoittaa annetyn ilmoituksen alueelle saavuttaessa
Esimerkki: exports['cc_modules']:InsertDistNotify(vector3(0, 0, 0), 2.5, 'Saavuit alueelle')

exports['cc_modules']:InsertBlip(name, scale, sprite, color, shortrange, coords)
Esimerkki: exports['cc_modules']:InsertBlip('Kauppa', 0.6, 59, 0, true, v.sij)
```

### Framework Modules (Server)
```markdown
exports['cc_logit']:logToDC(user, title, desc, webhook, color)
Esimerkki: exports['cc_logit']:logToDC('Yhteydet', 'Yhdistetään...', 'Pelaaja: **'..name..'**\nSteam: **'..steamid..'** \nRockstar License: **'..license..'** \nIP: **'..ip..'\n**Discord: **'..discord..'**', Logs.Yhteydet, 15105570)
```
