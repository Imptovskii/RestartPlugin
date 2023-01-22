# RestartPlugin

Оригинальный плагин был сделан: https://github.com/moom0o/RestartPlugin

На данный момент я сменил только с Bukkit.shutdown() на Bukkit.spigot().restart()

Так это без bash скрипта с автоперезапуском получается не авто рестарт, а авто выключение сервера.
Ну и добавил переменных которые используются в сообщениях при перезапуске сервера. Так как например две секунд, ну согласитесь звучит ну совсем инородно и глупо.

В будущем думаю довести до ума некоторые моменты. На данный момент как-то так.

```
# Minecraft restart notifications plugin by moo
# Time to where the server will call a restart
Timezone: "Europe/Moscow"
# THIS IS IN 24 HOUR TIME
RestartTimes:
  - "23:45:00" # 2AM EST
# - "14:00:00" #2PM EST

# %timeword% is the minute/seconds/second string.
# %time% is the number, ex: 15/10/5/2
string: "&e[SERVER] Сервер будет перезапущен через %time% %timeword%"
finalstring: "&e[SERVER] Сервер перезапускается..."
minutestring: "минут..."
minutesstring: "минуты..."
secondsstring: "секунд..."
alt-secondsstring: "секунды..."
secondstring: "секунду..."

# REBOOT AT LOW TPS SETTINGS
RebootFromLowTPS: true
TPSToStartCounting: 10
HowLongShouldTheServerGoWithLowTPS: 300 # seconds, the counter is reset if the server is above the specified tps for one second.
InstantRestart: false # Should the server send the 15 minute countdown messages?
```
