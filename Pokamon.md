```UML
@startuml
abstract class "Pokamon\nポカモン" as pokamon{
  -int power
  -int deffence
  -int hp
  -int maxHp
  -int speed
  -int criticalRate
  -boolean spAttackFlag
  -SecureRandom number
  -int spDeffect
  +int getPower()
  +int getDeffence()
  +int getHp()
  +int getSpeed()
  +int getCriticalRate()
  +boolean isSpAttackFlag()
  +int getTrueDeffence()
  +int getTotalParam()
  +boolean checkParameter()
  +boolean isAlive()
  +void doNormalAttack(Pokamon opp)
  +void doFullPowAttack(Pokamon opp)
  #void setSpAttackUsed()
  #void doDamaged(int damage)
  #int getDamage(int attack,Pokamon opp)
  #void recoverHp(int point)
  #void dispDamageMsg(Pokamon opp,int damage)
  #void setSpDeffenceInUse()
  {abstract} +String getName()
  {abstract} +boolean isSpecialAttack(int turn,int opHp,int opPow,int opDef)
  {abstract} +int getAttackType(int turn,int opHp,int opPow,int opDef)
  {abstract} +void execSpecialAttack(Pokamon opp)
  {abstract} +boolean isInSpAttack()
  {abstract} +boolean isInSpAttack()
  {abstract} +boolean isStrongFor(Pokamon opp)
  {abstract} +String getTypeName()
  {abstract} +boolean isRecoverHp()
  {abstract} #int getParamOffset()
  {abstract} #int getCriticalRateOffset()
}

class "PokamonEsper\n超タイプ" as pokamonEsper{
  +void execSpecialAttack(Pokamon opp)
  +boolean isRecoverHp()
  +String getTypeName()
  #int getParamOffset()
  #int getCriticalRateOffset()
  #boolean isInSpAttack()
  #boolean isStrongFor(Pokamon opp)
}

class "PokamonFire\n炎タイプ" as pokamonFire{
  +void execSpecialAttack(Pokamon opp)
  +boolean isRecoverHp()
  +String getTypeName()
  #int getParamOffset()
  #int getCriticalRateOffset()
  #boolean isInSpAttack()
  #boolean isStrongFor(Pokamon opp)
}

class "PokamonSteel\n鋼タイプ" as pokamonSteel{
  +void execSpecialAttack(Pokamon opp)
  +boolean isRecoverHp()
  +String getTypeName()
  #int getParamOffset()
  #int getCriticalRateOffset()
  #boolean isInSpAttack()
  #boolean isStrongFor(Pokamon opp)
}

class "PokamonVolt\n雷タイプ" as pokamonVolt{
  +void execSpecialAttack(Pokamon opp)
  +boolean isRecoverHp()
  +String getTypeName()
  #int getParamOffset()
  #int getCriticalRateOffset()
  #boolean isInSpAttack()
  #boolean isStrongFor(Pokamon opp)
}

class "PokamonWater\n水タイプ" as pokamonWater{
  +void execSpecialAttack(Pokamon opp)
  +boolean isRecoverHp()
  +String getTypeName()
  #int getParamOffset()
  #int getCriticalRateOffset()
  #boolean isInSpAttack()
  #boolean isStrongFor(Pokamon opp)
}

class "PolamonGrass\n草タイプ" as polamonGrass{
  +void execSpecialAttack(Pokamon opp)
  +boolean isRecoverHp()
  +String getTypeName()
  #int getParamOffset()
  #int getCriticalRateOffset()
  #boolean isInSpAttack()
  #boolean isStrongFor(Pokamon opp)
}

class "Main\nメインクラス" as main{
    -Pokamon blueFighters[]
    -Pokamon redFighters[]
    -int blueWinNum
    -int redWinNum
    -int drawNum
    -Scanner sc
  (static)+void main(String[] args)
  +void game()
  -boolean chkCheat()
  -void gameMain()
  -void oneGameMain(Pokamon blueFighter,Pokamon redFighter)
  -void getWinner(Pokamon blueFighter,Pokamon redFighter)
  -Pokamon[] getBattleTurn(Pokamon blueFighter,Pokamon redFighter)
  -boolean attack(int turn,Pokamon attack,Pokamon opp)
  -void dispStatus(Pokamon blueFighter,Pokamon redFighter)
  -void dispTitle()
  -void dispMember()
  -void waitEnter()
  -void dispWinTeam()
}

scale 1.5
pokamon <|-- pokamonEsper
pokamon <|-- pokamonFire
pokamon <|-- pokamonSteel
pokamon <|-- pokamonVolt
pokamon <|-- pokamonWater
pokamon <|-- polamonGrass
@enduml
```
