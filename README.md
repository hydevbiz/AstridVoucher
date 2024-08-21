## 🎫 AstridVoucher 

AstridVoucher is a plugin designed to manage and distribute vouchers on your Minecraft server. It allows you to easily grant players vouchers with various rewards and configurations.

### 🔧 Commands

- **`/voucher give <voucher_name> %player_name% <quantity>`**
  - **Description:** Grants a specified number of vouchers to a player.
  - **Usage Example:** `voucher give rankknight player123 1`

### ⚙️ Example Configuration 

Here are examples of different voucher types you can set up with the `AstridVoucher` plugin:

#### Normal Voucher

This voucher grants a rank or permission to the player.

#### Normal Voucher Configuration

```yaml
rankknight:
  material: 'PLAYER_HEAD'
  skull-url: "http://textures.minecraft.net/texture/55a5e142a889d73a0dc4e95343de2689549d23ac77edb9a7ec127839d4973cbf"
  name: '&3&k|&3Knight&3&k|&r &3&lRank Voucher'
  glow: false
  lore:
    - '&7This voucher grants &afree &7access'
    - '&7to the &3&k|&3Knight&3&k|&r &7rank!'
    - ''
    - '&a&lRight Click&r&7 to redeem'
  fireworks: []
  sounds:
    - 'ENTITY_ITEM_PICKUP;1.0;1.0'
  commands:
    - 'lp user {player} parent addtemp knight 30d'
```

#### Chance Voucher Configuration

```yml

kitknight:
  material: PAINTING
  name: '&3&k|&3Knight&3&k|&r &3&lKit Voucher'
  glow: true
  lore:
    - '&7This voucher gives you access to'
    - '&7all the items in the &3&k|&3Knight&3&k|&r &7kit.'
    - '&7Gearing up has never been easier!'
    - ''
    - '&a&lRight Click&r&7 to redeem'
  fireworks: []
  sounds:
    - 'ENTITY_ITEM_PICKUP;1.0;1.0'
  rewards:
    main:
      name: Knight Set!
      chance: 100
      commands:
        - 'ak give {player} kit ranked_knight_kit 1'
        - 'ak give {player} kit ranked_knight_once 1'
  animation:
    enabled: true
    text: "<gold><obfuscated>A <!obfuscated><white>%item% <yellow><obfuscated>A"
    sub-text: "Knight Kit Voucher"
    fade-in: 0
    stay: 20
    fade-out: 5
    direction: RIGHT_TO_LEFT
    update-ticks: 20
    color-after-randomization: "&a"
```

## 🛠️ Custom Skull Head Support 
AstridVoucher supports custom skull heads. You can use a URL for the skull texture or specify a material type. Customize the skull-url or material field to use custom textures for your vouchers.
