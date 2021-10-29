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
  {final} +int getPower()
  {final} +int getDeffence()
  {final} +int getHp()
  {final} +int getSpeed()
  {final} +int getCriticalRate()
  {final} +boolean isSpAttackFlag()
  {final} +int getTrueDeffence()
  {final} +int getTotalParam()
  {final} +boolean checkParameter()
  {final} +boolean isAlive()
  {final} +void doNormalAttack(Pokamon opp)
  {final} +void doFullPowAttack(Pokamon opp)
  {final} #void setSpAttackUsed()
  {final} #void doDamaged(int damage)
  {final} #int getDamage(int attack,Pokamon opp)
  {final} #void recoverHp(int point)
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
  {final} +void execSpecialAttack(Pokamon opp)
  {final} +boolean isRecoverHp()
  {final} +String getTypeName()
  {final} #int getParamOffset()
  {final} #int getCriticalRateOffset()
  {final} #boolean isInSpAttack()
  {final} #boolean isStrongFor(Pokamon opp)
}

class "PokamonFire\n炎タイプ" as pokamonFire{
  {final} +void execSpecialAttack(Pokamon opp)
  {final} +boolean isRecoverHp()
  {final} +String getTypeName()
  {final} #int getParamOffset()
  {final} #int getCriticalRateOffset()
  {final} #boolean isInSpAttack()
  {final} #boolean isStrongFor(Pokamon opp)
}

class "PokamonSteel\n鋼タイプ" as pokamonSteel{
  {final} +void execSpecialAttack(Pokamon opp)
  {final} +boolean isRecoverHp()
  {final} +String getTypeName()
  {final} #int getParamOffset()
  {final} #int getCriticalRateOffset()
  {final} #boolean isInSpAttack()
  {final} #boolean isStrongFor(Pokamon opp)
}

class "PokamonVolt\n雷タイプ" as pokamonVolt{
  {final} +void execSpecialAttack(Pokamon opp)
  {final} +boolean isRecoverHp()
  {final} +String getTypeName()
  {final} #int getParamOffset()
  {final} #int getCriticalRateOffset()
  {final} #boolean isInSpAttack()
  {final} #boolean isStrongFor(Pokamon opp)
}

class "PokamonWater\n水タイプ" as pokamonWater{
  {final} +void execSpecialAttack(Pokamon opp)
  {final} +boolean isRecoverHp()
  {final} +String getTypeName()
  {final} #int getParamOffset()
  {final} #int getCriticalRateOffset()
  {final} #boolean isInSpAttack()
  {final} #boolean isStrongFor(Pokamon opp)
}

class "PolamonGrass\n草タイプ" as polamonGrass{
  {final} +void execSpecialAttack(Pokamon opp)
  {final} +boolean isRecoverHp()
  {final} +String getTypeName()
  {final} #int getParamOffset()
  {final} #int getCriticalRateOffset()
  {final} #boolean isInSpAttack()
  {final} #boolean isStrongFor(Pokamon opp)
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

pokamon <|-- pokamonEsper
pokamon <|-- pokamonFire
pokamon <|-- pokamonSteel
pokamon <|-- pokamonVolt
pokamon <|-- pokamonWater
pokamon <|-- polamonGrass
@enduml
```
