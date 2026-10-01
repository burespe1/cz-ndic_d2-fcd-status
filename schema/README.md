# Schéma cz-ndic_d2-fcd-status-v2.0

XSD se generuje ve webtool.datex2.eu z `sel/cz-ndic_d2-fcd-status.sel` (DATEX II 3.7). Vstupní soubor `DATEXII_3_D2Payload.xsd`.

* Nevybírat balíčky CommonExtension / LocationExtension (mění typy _…Extension).
* Rozšíření NDIC (FCD) je samostatné, ručně psané XSD `cz-ndic_d2-fcd-extension-1.0.xsd` v namespace `http://ndic.cz/datex2/fcd/extension/1.0` (stupeň provozu, kolony). Uvedeno ve `FORMAT.yaml` (`schema.extensions`), `d2doc check` proti němu validuje vzorky. Webtool ho nepřepisuje.
* Hodnoty výčtů: webtool je zapíše do `.sel` jen tehdy, je-li ve výčtu některá hodnota odznačena. Výběr obsahuje zúžené výčty VehicleTypeEnum, TrafficStatusEnum, ConfidentialityValueEnum a InformationStatusEnum. `_VehicleTypeEnumExtensionType` (rozšíření výčtu úrovně A) v XSD zůstává i po zúžení – výběr ho neovlivní.
