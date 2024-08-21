## AstridVoucher

### Commands

- **`voucher give <voucher_name> %player_name% <quantity>`**
  - **Description:** Grants a specified quantity of a voucher to a player.
  - **Usage Example:** `voucher give rankknight player123 1`

### Example Configuration

Below are examples of different types of vouchers you can configure for the `AstridVoucher` plugin:

#### Normal Voucher

This voucher provides a rank or permission to the player.

```yaml
# Normal Voucher Configuration
rankknight:
  material: 'PLAYER_HEAD'
  skull-url: "http://textures.minecraft.net/texture/55a5e142a889d73a0dc4e95343de2689549d23ac77edb9a7ec127839d4973cbf"
  name: '&3&k|&3Knight&3&k|&r &3&lRank Voucher'
  glow: false
  lore:
    - '&7This voucher will give you &afree &7access'
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
  name: '&3&k|&3Knight&3&k|&r &3&lkit Voucher'
  glow: true
  lore:
    - '&7Incredible, this gives you access to all'
    - '&7the items included in the &3&k|&3Knight&3&k|&r &7kit.'
    - '&7Gearing up has never been that easy!'
    - ''
    - '&a&lRight Click&r&7 to redeem'
  fireworks: []
  sounds:
    - 'ENTITY_ITEM_PICKUP;1.0;1.0'
  rewards:
    main:
      name: Knight set!
      chance: 100
      commands:
        - 'ak give {player} kit ranked_knight_kit 1'
        - 'ak give {player} kit ranked_knight_once 1'
  animation:
    enabled: true
    text: "<gold><obfuscated>A <!obfuscated><white>%item% <yellow><obfuscated>A"
    sub-text: "Knight kit voucher"
    fade-in: 0
    stay: 20
    fade-out: 5
    direction: RIGHT_TO_LEFT
    update-ticks: 20
    color-after-randomization: "&a"
```

# Custom Skull Head Support

The AstridVoucher plugin supports custom skull heads. You can use a URL for the skull texture or specify a material type. Customize the skull-url or material field to use custom textures for your vouchers.
