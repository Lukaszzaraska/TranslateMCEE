# TranslateMCEE
**Tłumaczenie samouczków do wbudowanej mapy w MC EE (funkcje)**
- T1 --> poziom nowicjusz
- T2 --> poziom zaawansowany
- T3 --> poziom ekspert

1. Stwórz plik z rozszerzeniem .md 
2. Umieść nazwe pliku w pxt.json
3. Zmodyfikuj link w plikach gry (blocks.mcfunction)

W plikach danego świata:
\behavior_packs\bp0\functions

Przykład linku:
http://minecraft.makecode.com/#tutorial:https://github.com/LukaszZaraska/TranslateMCEE/agent_fun_blocks_T

**Tworzenie samouczków połączonych z githubem**<br>
Wpisujemy komende u npc

przykład samouczka z którego można wyjść
execute @p ~ ~ ~ codebuilder navigate @s false http://minecraft.makecode.com/#tutorial:https://github.com/Lukaszzaraska/TranslateMCEE/MC2_17/zad1

Przykład zablokowanego samouczka
execute @p ~ ~ ~ codebuilder navigate @s false http://minecraft.makecode.com//?lockedEditor=1#tutorial:https://github.com/Lukaszzaraska/TranslateMCEE/MC2_17/zad1

Po edycji na githubie pliku należy poczekać pare minut zanim zacznie działać <br>
?? Prawdopodobnie dodawanie nazw plików w pxt.json gdy dane pliki jeszcze nie istnieją LUB dodanie kilku nazw naraz w jednym commitsie powoduje przestanie działanie wszystkich plików
