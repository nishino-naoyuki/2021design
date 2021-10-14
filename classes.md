```UML
@startuml
abstract class "Creature\n生物" as creature{
  -String name
  -int hp
  {abstract} #void attack(Creature opponent)
  +void damaged(int damage)
  +boolean isAlive()
  +String getName()
  +int getHp()
  #void displayMessage(Creature opponent,int damage)
}
class "Braver\n勇者" as braver{
}
abstract class "Monster\nモンスター" as monster{
}
class "Slime\nスライム" as slime{
}
class "Wizard\n魔法使い" as wizard{
}
class "MetalSlime\nメタルスライム" as metalSlime{
}

creature <|-- braver
creature <|-- monster
monster <|-- slime
monster <|-- wizard
monster <|-- metalSlime
@enduml
```
