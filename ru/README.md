# Sponjik RU services (rule-sets)

Домены российских сервисов (~1242, 46 категорий) — для маршрутизации в mihomo.
Назначение: рос-сервисы → DIRECT (реальный ру-IP, не палим VPN, не ловим баны).

## Файлы
- `ru-all.mrs` — все домены одним rule-set.
- `ru-<категория>.mrs` — по категориям (banks, gov, streaming, gaming, game_dev, ...).
- `_source/sponjik-ru-services.txt` — исходник по категориям (для пересборки).

## Использование (rule-provider, behavior: domain, format: mrs)
    ru-services:
      type: http
      behavior: domain
      format: mrs
      proxy: 🌍 VPN
      url: https://github.com/VolodyaMEGAlodon/Sponjik_Mihomo_Rules/raw/main/ru/ru-all.mrs
      path: ./rule-sets/ru-services.mrs
      interval: 86400
    # rules:
    #   - RULE-SET,ru-services,DIRECT
