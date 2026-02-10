---
level: 1
class: TODO
subclass: TODO
race: TODO
subrace: TODO
HP: TODO
speed: 30ft
proficiency_bonus: 2
character_name: TODO
background: TODO
size: TODO
str: "10"
dex: "10"
con: "10"
int: "10"
wis: "10"
cha: "10"
hit_dice: d10
alignment: TODO
---
# Character
```stats
items:
  - label: Name
    value: '{{frontmatter.character_name}}'
```
![[TODO]]
```stats
items:  
  - label: Race
    sublabel: '{{frontmatter.subrace}}'
    value: '{{frontmatter.race}}'
  - label: Class
    sublabel: '{{frontmatter.subclass}}'
    value: '{{frontmatter.class}} {{ frontmatter.level }}'
  - label: Background
    value: '{{frontmatter.background}}'
  - label: Size
    value: '{{frontmatter.size}}'


grid:
  columns: 2
dense: true
```
## Description

| Age | Height | Weight | Eyes | Skin | Hair |
| --- | ------ | ------ | ---- | ---- | ---- |
|     |        |        |      |      |      |

## Personality
```stats
items:  
  - label: Alignment
    value: '{{frontmatter.alignment}}'
```
>[!info] Traits
>TODO

>[!info] Ideals
>TODO

>[!info] Bonds
>TODO

>[!info] Flaws
>TODO
## Backstory
TODO
# Stats
```stats
items:
  - label: Armor Class
    sublabel: TODO
    value: '{{10 TODO}}' 
  - label: Initiative
    value: '+{{ modifier abilities.dexterity }}'
  - label: Speed
    sublabel: walk
    value: '{{frontmatter.speed}}'
  - label: Passive Perception
    value: '{{add 10 (modifier abilities.wisdom)}}'
  - label: Senses
    value: TODO
grid:
  columns: 5
dense: true
```

```ability
abilities:
  strength: '{{frontmatter.str}}'
  dexterity: '{{frontmatter.dex}}'
  constitution: '{{frontmatter.con}}'
  intelligence: '{{frontmatter.int}}'
  wisdom: '{{frontmatter.wis}}'
  charisma: '{{frontmatter.cha}}'
  
bonuses:
  - name: TODO
    target: 
    value: 
    modifies: 

proficiencies:
```

```skills
proficiencies:
  
expertise:
```
```consumable
items:
  - label: "Inspiration"
    state_key: inspiration
    uses: 1
    reset_on:
      - event: long-rest  # Full reset on long rest
```
# HP
```healthpoints
state_key: my_character_hp
health: '{{frontmatter.HP}}'
hitdice:
  dice: '{{frontmatter.hit_dice}}'
  value: '{{frontmatter.level}}'
```
# Action
```stats
items:
  - value: TODO
  - label: Attack
    value: '+{{add (modifier abilities.TODO) frontmatter.proficiency_bonus }}'
  - label: Damage
    sublabel: TODO
    value: '1dX+{{modifier abilities.TODO}}'
  - label: Reach
    value: TODO ft
  - label: Mastery
    value: TODO
grid:
  columns: 5
dense: true
```
# Privileges and traits

> [!danger] TODO
> ```consumable
> items:
>   - label: "uses"
>     state_key: unique_id
>     uses: 1
>     reset_on:
>       - event: long-rest  # Full reset on long rest
>       - event: short-rest
>         amount: 1
> ```
> Description
## Proficiencies
### Languages
```badges
items:
  - value: TODO
  - value: TODO
  - value: TODO
```
### Armor: 
```badges
items:
  - value: Light
  - value: Medium
  - value: Heavy
```
### Weapon:
```badges
items:
  - value: Martial
  - value: Simple
```
## Feats

# Inventory
## Purse

| CP  | SP  | EP  | GP  | PP  |
| --- | --- | --- | --- | --- |
|     |     |     |     |     |
## Attuned Objects
- TODO
- TODO
- TODO
## Objects
# Spells
```badges
items:
  - label: Spell Ability
    value: TODO
  - label: DC
    value: '{{add 8 frontmatter.proficiency_bonus (modifier abilities.TODO) }}'
  - label: Modifier
    value: '+{{ modifier abilities.TODO }}'
  - label: Attack Bonus
    value: '+{{add frontmatter.proficiency_bonus (modifier abilities.TODO)}}'
```
```consumable
items:
  - label: "Level 1 Spells"
    state_key: my_character_spells_1
    uses: 4
    reset_on: "long-rest"
  - label: "Level 2 Spells"
    state_key: my_character_spells_2
    uses: 2
    reset_on: "long-rest"
```

>[!note] Booming Blade
>```badges
>items:
>  - label: cantrip # level
>  - label: evocation # school
>```
>  
>```spell-components
>casting_time: 1 action
>range: self (5ft)
>components: S, M (melee weapon 1SP)
>duration: Instantaneous
>```
>TODO