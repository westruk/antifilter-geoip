# Назначение

Форк оригинального проекта для сборки dat-файлов IP для проектов V2Fly, XRay и подобных на основе списков [Antifilter](https://antifilter.download/)
Сборка проводится автоматически ежедневно через GitHub Actions

## Использованные списки
- Файл ```geoip.dat``` собирается на основе списка <https://antifilter.download/list/allyouneed.lst>

## Ссылки на скачивание

- **geoip.dat**：<https://github.com/schebotar/antifilter/releases/latest/download/geoip.dat>

## Пример использования

```json
{
  "routing": {
      "rules": [
      {
        "ip": [
          "ext:geoip.dat:antifilter"
        ],
        "type": "field",
        "outboundTag": "proxy"
      },
      {
        "type": "field",
        "outboundTag": "direct"
      }
    ]
  }
}
```
