### @explicitHints 1

# Lesson 1: Code a Road Network

## Step 1
Переименуйте текст **run** в блоке ``||Player:on chat command||`` на  **дорога**. Выберите блок ``||Blocks:fill with||`` и вставьте его внутрь вашего блока ``||Player:on chat command||``.

### ~ tutorialhint
``` blocks
player.onChat("road_1", function () {
    blocks.fill(
    GRASS,

    pos(0, 0, 0),
    pos(0, 0, 0),
    FillOperation.Replace
    )
})
```

## Step 2
Используйте всплывающее меню, чтобы заменить **Траву** to **Серый бетон**.
### ~ tutorialhint

``` blocks
player.onChat("road_1", function () {
    blocks.fill(
    GRAY_CONCRETE,
    pos(0, 0, 0),
    pos(0, 0, 0),
    FillOperation.Replace
    )
})
```

## Step 3
Откройте блок ``||Positions:POSITIONS||`` и возмите блок ``||Positions:[0] [0] [0]||``. Затем замените им первую строку блока ``||Blocks:fill||``.

### ~ tutorialhint
``` blocks
player.onChat("road_1", function () {
    blocks.fill(
    GRAY_CONCRETE,
    world(0, 0, 0),
    pos(0, 0, 0),
    FillOperation.Replace
    )
})
```

## Step 4
Возьмите еще один блок ``||Positions:world [0] [0] [0]||`` и замените им вторую строку блока ``||Blocks:fill with||``.

### ~ tutorialhint
``` blocks
player.onChat("road_1", function () {
    blocks.fill(
    GRAY_CONCRETE,
    world(0, 0, 0),
    world(0, 0, 0),
    FillOperation.Replace
    )
})
```

## Step 5
Мы почти готовы протестировать наш код, однако есть еще одна важная вещь, которую мы должны сделать, чтобы этот код работал должным образом. Замените центральную, или **Y** координату, на число ниже. В этом примере это будет **68**. Теперь протестируйте свой код. Если вы закодировали правильно, вы должны увидеть, что вместо травы появилась дорога.

### ~ tutorialhint
``` blocks
player.onChat("road_1", function () {
    blocks.fill(
    GRAY_CONCRETE,
    world(-21, 68, -565),
    world(61, 68, -569),
    FillOperation.Replace
    )
})

```

## Step 6
Повторите шаги для второй дороги.

### ~ tutorialhint
``` blocks
player.onChat("road_2", function () {
    blocks.fill(
    GRAY_CONCRETE,
    world(-21, 68, -532),
    world(61, 68, -536),
    FillOperation.Replace
    )
})
```

## Step 7
Дополнительно. Сделав две дороги, постройте еще, используя только что созданный код. Когда вы закончите, подойдите к NPC из раздела 2 Урок 1 и попросите немного ковра, чтобы нанести дорожную разметку с помощью вашего агента для ее размещения.
