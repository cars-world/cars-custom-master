<!--
@license
Copyright (c) rljson

Use of this source code is governed by terms that can be
found in the LICENSE file in the root of this package.
-->

# Das Image in crcars bauen

## Motivation

- cars-custom-master ist der Master der Seite custom, in der freigegebene
  Kataloge für Kunden weiterbearbeitet werden; bisher antwortet er mit
  einem Gruß
- Die Registry und die Stufen hatten neue Namen: eine Registry `crcars`
  für alle Stufen statt einer je Stufe, und die Stufen `dev`, `test` und
  `prod`

## Strategie

- Nur die README ändern; der Code bleibt, wie er ist

## Image und Stufen

- Die README baut das Image mit
  `az acr build --registry crcars --image cars-custom-master:<version> .`
- Sie nennt die Stufen `dev`, `test` und `prod` und sagt, dass der Master
  in jeder als Container läuft, auch hinter einem Proxy, der ihn unter
  einem Pfad ausliefert und das Präfix entfernt

## Ergebnis

- `cars-custom-master:0.0.1` liegt in `crcars` und antwortet
  `Hello from cars-custom-master`

## Offene Punkte

- Der Master hält noch keine Daten
