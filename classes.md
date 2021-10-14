```UML
@startuml
abstract class "Creature\n生物" as creature{
  -String name
  -int hp
  {abstract} +void attack(Creature opponent)
  +void damaged(int damage)
  +boolean isAlive()
  +String getName()
  +int getHp()
  #void displayMessage(Creature opponent,int damage)
}
class "Braver\n勇者" as braver{
  +void attack(Creature opponent)
  +void recovery()
}
abstract class "Monster\nモンスター" as monster{
  #boolean escapeFlag
  +void displayAppearanceMsg()
  +boolean isEscaped()
  +boolean isThere()
}
class "Slime\nスライム" as slime{
  +void attack(Creature opponent)
}
class "Wizard\n魔法使い" as wizard{
  +void attack(Creature opponent)
}
class "MetalSlime\nメタルスライム" as metalSlime{
  +void attack(Creature opponent)
}

class "RPGMain\nメインクラス" as main{
  -Braver braver
  -Monster[] monsters
  (static)+void main(String[] args)
  +void game()
  -void dispTitle()
  -void dispBattleStart()
  -void dispStatus()
  -void dicideMonsters()
  -boolean battle()
  -boolean isNotThereAllMonster()
}

creature <|- braver
creature <|- monster
monster <|- slime
monster <|- wizard
monster <|- metalSlime
@enduml
```
