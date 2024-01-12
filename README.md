# CloudRelog API

```java
RelogMain relogMain = (RelogMain) Bukkit.getPluginManager().getPlugin("CloudRelog");
RelogAPI = relogMain.getAPI
```
# Методы

1. Находится ли игрок в режиме PvP:
```java
public boolean isInPvP(Player player);
```

2. Начать PvP для двух игроков с определенным временем:
```java
public void startPvP(Player player, Player damager, int cooldown);
```

3. Начать PvP для двух игроков с временем из конфига:
```java
public void startPvP(Player player, Player damager);
```

4. Начать PvP между игроками, игнорируя проверки на God, Fly, Vanish, GameMode, а также на то, находятся ли они уже в PvP:
```java
public void startPvPIgnoreChecks(Player player, Player damager, int cooldown);
```

5. Начать PvP только для одного игрока
```java
public void startAlonePlayer(Player player, int cooldown);
```

6. Запустить вечный режим PvP для одного игрока:
```java
public void startInfinityPvP(Player player);
```

7. Принудительная остановка PvP для одного игрока:
```java
public void stopPvP(Player player);
```

8. Получение текущего BossBar у игрока. Может вернуть null:
```java
public BossBar getPlayerBossBar(Player p);
```

9. Возвращает класс PvPCooldown (информация о текущем остатке времени КТ) для игрока. Две переменные: remaining(остаток) и maximum(изначальное время):
```java
public PvPCooldown getPlayerCooldown(Player p);
```
