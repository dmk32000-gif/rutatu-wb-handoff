# Unit Economics Completion Plan

_Сгенерировано автоматически. Дата: 2026-04-20._
_Показывает все 170 placeholder SKU (значение = 50.0) и план их обновления._

## Сводка

- Всего placeholder SKU: **170**
- can_estimate_from_reports: **yes** (WB_API_TOKEN_ANALYTICS доступен → reportDetailByPeriod содержит комиссию и логистику по SKU)
- requires_manual_cogs: **yes (все SKU)** — себестоимость никогда не приходит из WB API

## Порядок действий

1. Запустить скрипт синхронизации reportDetailByPeriod → получить комиссию и логистику по SKU
2. Заполнить `data/input/cogs.csv` — себестоимость для каждого SKU (ручной ввод)
3. Пересчитать `unit_economics.csv`: profit = price − commission − logistics − storage − cogs − tax

## Таблица по SKU

| sku | product_name | packaging_profile | current_value | can_estimate_from_reports | requires_manual_cogs | recommended_step |
|---|---|---|---|---|---|---|
| 026-6X8-MAK | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 028-12X16-PEONY | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 030-16X24-FLOWER | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 031-6X8-BUTON | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 033-8X12-PEONY | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 034-12X16-PEONIES | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 037-6X8-POPUGAI | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 038-6X8-SOVA | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 039-8X12-PEACOCK | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 040-8X12-TUKAN | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 041-12X16-HUMMINGBIRD | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 043-16X48-JAPANESE | Временные татуировки и стразы | unknown | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 046-6X8-EDINOROG | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 047-6X8-SKULL | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 048-8X12-LION | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 052-12X16-DOODLE | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 053-6X8-FLAG | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 057-6X8-FOOTBAL | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 059-6X8-LADYBAGS | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 060-6X8-PINEAPPLE | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 065-6X8-RYBKA | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 066-6X8-NEMO | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 067-8X12-SEAHORSE | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 068-12X16-FISH | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 083-6X8-KAKTUS | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 086-12X16-JUNIPER | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 097-12X16-LOTUS | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 099-16X24-MASK | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 102-16X24-JOKER | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 103-6X8-MEHENDI | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 104-6X8-MANDALA | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 105-8X12-HAMSA | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 111-16X48-ZEBRA | Временные татуировки | unknown | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 114-17X5-PINK | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 120-16X24-BRUISES | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 124-10X48-BRANCH-BERRIES | Временные татуировки и стразы | unknown | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 125-6X8-KOFE | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 126-6X8-BUCHLAVKA | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 127-8X12-WINE | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 128-12X16-WINE-CAT | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 136-17X5-YAGODKI | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 137-17X5-LIGHT | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 138-17Х5-PINK | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 140-6X8-BABOCHKA | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 141-6X8-PION | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 142-8X12-PEONY | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 157-8X24-CHAIN | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 158-8X24-VINTAGE | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 160-8X12-OWL | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 175-16X24-LOTUS | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 238-12X16-FISH | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 271-24X32-SNAKE | Временные татуировки и стразы | unknown | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 274-6X16-SNAKE | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 282-6Х16-RADUGA | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 284-12Х16-AMONGUS | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 285-12Х16-MASHINKI | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 286-6Х16-MEDVEDI | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 287-12Х16-DRAKONI | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 288-6Х16-KARAKULI | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 296-6X8-CHERNAYA-METKA | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 299-8X12-PAUKI | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 307-8X12-MONKEY | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 308-8X12-FISH | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 317-8X12-HEARTS | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 319-8X12-ANIMAL | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 332-12Х16-IGRA-KALMARA | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 334-6Х16-PERO | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 336-6Х16-ALFAVIT | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 339-16X48-LILY | Тату-рукава | unknown | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 351-16X24-TIGER | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 398-6X16-TOCHKA | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 463-8Х12-TSVETI | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 463-8Х12-TSVETI/PIC | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 470-16X48-SLEEVE | Временные татуировки и стразы | unknown | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 472-6Х16-KRISTALLI | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 473-8Х12-RIBKI | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 474-16X24-BLACKWORK | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 476-8X12-OSMINOG | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 499-12X16-ESHER-PEEL | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| 507-12Х32-FLOWERS-TENDERNESS | Временные татуировки и стразы | unknown | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCAT462-12X16-MI | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCAT6Х380-6X8-3CATS-CARAMEL | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCAT6Х381-6X8-3CATS-CORZHIK | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCAT6Х382-6X8-3CATS-COMPOTE | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCAT6Х383-6X8-3CATS-SAZHIK | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCAT6Х384-6X8-3CATS-GORCHITSA | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCAT6Х385-6X8-3CATS-LAPOCHKA | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCAT6Х388-6X8-3CATS-SHURUP | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCAT6Х390-6X8-3CATS-CARAMELKA-SNOW | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCAT6Х392-6X8-3CATS-CARAMELKA | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCAT6Х393-6X8-KORZHIK | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCAT6Х395-6X8-3CATS-LAPOCHKA | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCAT8Х450-8X12-3CAT-JAPAN | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCAT8Х451-8X12-3CAT-KNIGHTS | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCAT8Х454-8X12-3CAT-MUSICIANS | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCAT8Х455-8X12-3CAT-MASQUERADE | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCAT8Х456-8X12-3CAT-DIVING | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCHLD227-6X16-MONSTER | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCHLD228-6X16-EDINOROG | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCHLD231-6X16-DOG | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCHLD232-6X16-CAT | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCHLD234-6X16-ANIMAL | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUFLWR273-6X16-WATERCOLOUR | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUINS267-6X16-TAT | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUKIDS307-8X12-MONKEY | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUKIDS309-8X12-DOGS | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUKIDS314-8X12-SNAIL | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUKIDS315-8X12-GIRAF | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUKIDS316-8X12-SPACE | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUKIDS318-8X12-PIRATES | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUKIDS319-8X12-ANIMAL | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUKIDS321-8X12-DINO | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUKIDS330-8X12-EDINOROG | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUMIN001-6X8-MAP | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUMIN002-6X8-TREBLE | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUMIN003-6X8-STARS | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUMIN005-6X8-HEARTS | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUMIN006-6X8-CROWN | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUMIN007-6X8-INFINITY | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUMIN008-6X8-PINEAPPLE | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUMIN009-6X8-LOTUS | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUMIN010-6X8-BARCODE | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUMIN011-6X8-AND | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUMIN012-6X8-HUMMINGBIRD | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUMIN013-6X8-PAW | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUMIN014-6X8-ORIGAMI | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUMIN015-6X8-AIRPLANE | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUMIN016-6X8-CROSS | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUMIN017-6X8-DEATHLY | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUMIN018-6X8-DIAMOND | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUMIN019-6X8-FLOWER | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUMIN020-6X8-NOTES | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUMIN022-6X8-SUN | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUMIN023-6X8-PLAYER | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUNBT084 | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUNBT115 | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUNBT343-17X5-WOLF | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUNBT344-6X16-CAT | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUNBT345-6X16-LEV | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUNBT346-6X16-LEOPARD | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUNBT348-6X16-PANTHER | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUNBT350-6X16-HUSKY | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUPAL197-6X16-ANTS | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUPLS117-12X16-NADPISI | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUPLS213-12X16-RABBIT | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUPLS268-12X16-OLD-SCHOOL | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUSML266-6X8-SKULL | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUANI193-12X16-LION-LOTUS | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUBUT241-8X24-DRAGON | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCRT323-12X16-ROSE | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCRT325-12X16-CROCUS | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUCRT329-12X16-BABOCHKA | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUEAS185-12X16-ZHASMIN | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUGEO367-8X12-WOLF | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUGEO369-8X12-TIGER | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUGEO370-8X12-PANTHER | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUGEO371-8X12-LYNX | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUGEO372-8X12-LION | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUGEO373-8X12-UNICORN | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUGEO374-8X12-BUTTERFLY | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUGEO377-8X12-FOX | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUHND223-8X12-FOUR | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUMEH204-16X24-PCHELA | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUORN171-8X24-ORNAMENT | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUORN172-8X24-MANDALA | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUSLV225-16X48-SAPPHIRES | Временные татуировки | unknown | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| RUTATUSNK363-16X24-SNAKE | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| NAROZI480-6Х8-YA-TEBYA-LUBLU | Временные татуировки и стразы | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| NAROZI481-6Х8-ILOVEU | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
| NAROZI484-6Х8-KRASH | Временные татуировки | tattoo_packet | 50.0 | yes (reportDetailByPeriod) | yes | Получить из API + ручной COGS |
