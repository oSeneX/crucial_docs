## Crucial Framework documentation

### Framework Functions

####Client:
```markdown
- 
```
####Server:
```markdown
local player = exports['cc_base']:GetPlayer(source)
player.setdeathStatus(status) -- 0 = elävä 1 = kuollut
player.getdeathStatus() 
player.getPos() 
player.getChar() -- Valittu hahmo (1 & 2)
player.addItem(name, count) -- Itemit sekä aseet
player.removeItem(name, count)
player.weaponAmmo(name, count, val) -- val = true antaa ammuksia, val = false poistaa ammuksia
player.getJob() 
player.giveJob()
player.getDuty()
player.getIdentifier()
player.getGroup()
player.giveGroup(group)
player.getBank() -- Pankkilillä oleva summa
player.getAccountNumber() -- Pankkitilin tilinumero
player.getSecondaryBank() -- Säästötilillä oleva summa
player.getSecondAccountNumber() -- Säästötilin tilinumero
player.giveBank(amount)
player.giveSecondaryBank(amount)

**Items**
player.getItemLabel(item)
player.getItemType(item) -- Item or weapon
player.getItemWeight(item) -- in grams
player.getItemDurability(item) -- Max durability
player.isItemUsable(item)
```

####Callbacks:
```markdown
**Client:**
exports['cc_base']:TriggerServerCallback('eventName', function() end)

**Server:**
exports['cc_base']:RegisterCallback('eventName', function(source, cb) end)
```

### Framework Modules
```markdown
**Client:**
exports['cc_modules']:InsertDistNotify(coords, distance, notifyteksi) -- Ilmoittaa annetyn ilmoituksen alueelle saavuttaessa
Esimerkki: exports['cc_modules']:InsertDistNotify(vector3(0, 0, 0), 2.5, 'Saavuit alueelle')

exports['cc_modules']:InsertBlip(name, scale, sprite, color, shortrange, coords)
Esimerkki: exports['cc_modules']:InsertBlip('Kauppa', 0.6, 59, 0, true, v.sij)

**Server:**
```
