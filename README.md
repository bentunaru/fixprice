# CME Fix Price Indicator - PineScript v6

Indicateur TradingView pour détecter et tracer les niveaux de fix price (limites de prix) du CME.

## Description

Cet indicateur PineScript v6 détecte automatiquement lorsque le prix atteint les niveaux de limite du CME (communément utilisés pour les contrats futures sur indices boursiers comme l'E-mini S&P 500) et trace une ligne horizontale au prix de fix.

## Fonctionnalités

### Niveaux de Limite
- **Niveau 1** : 7% par défaut (pause de trading de 15 minutes)
- **Niveau 2** : 13% par défaut (pause de trading de 15 minutes)
- **Niveau 3** : 20% par défaut (arrêt du trading pour la journée)

### Caractéristiques
- ✅ Détection automatique des niveaux de limite atteints
- ✅ Ligne horizontale tracée au prix exact de fix
- ✅ Étiquettes informatives avec le niveau et le prix
- ✅ Prix de référence configurable (clôture précédente, ouverture de session, ou personnalisé)
- ✅ Couleurs personnalisables pour chaque niveau
- ✅ Alertes configurables pour chaque niveau de limite
- ✅ Réinitialisation automatique chaque jour

### Affichage
- Lignes pointillées pour les niveaux de limite (haut et bas)
- Ligne solide au prix de fix quand un niveau est atteint
- Ligne bleue pour le prix de référence
- Extension de la ligne vers la droite pour suivre le prix

## Installation

1. Ouvrir TradingView
2. Cliquer sur "Éditeur Pine" en bas de l'écran
3. Copier le contenu du fichier `fix_price_indicator.pine`
4. Coller dans l'éditeur Pine
5. Cliquer sur "Ajouter au graphique"

## Configuration

### Prix de Référence
- **Previous Close** : Utilise la clôture du jour précédent (recommandé pour CME)
- **Session Open** : Utilise l'ouverture de la session actuelle
- **Custom** : Permet de définir manuellement un prix de référence

### Paramètres des Limites
Ajustez les pourcentages selon l'instrument tradé :
- Pour les indices boursiers (ES, NQ) : 7%, 13%, 20%
- Pour d'autres instruments : ajustez selon les règles du CME

### Affichage
- Activez/désactivez chaque niveau individuellement
- Ajustez l'épaisseur des lignes (1-5)
- Activez/désactivez les étiquettes
- Personnalisez les couleurs pour chaque niveau

### Alertes
Configurez des alertes pour être notifié :
- "Fix Price Level 1" : Niveau 1 atteint
- "Fix Price Level 2" : Niveau 2 atteint
- "Fix Price Level 3" : Niveau 3 atteint
- "Fix Price Triggered" : N'importe quel niveau atteint

## Utilisation

1. **Appliquer l'indicateur** sur votre graphique de futures (ES, NQ, etc.)
2. **Vérifier le prix de référence** (ligne bleue) correspond bien à la clôture précédente
3. **Observer les niveaux de limite** (lignes pointillées colorées)
4. **Attendre la détection** : Quand un niveau est atteint, une ligne solide apparaît
5. **Lire l'étiquette** pour connaître le niveau exact et le type (UP/DOWN)

## Exemple de Lecture

```
FIX PRICE
Level 2 UP
4850.50
```
Signifie que le prix a atteint le niveau 2 de limite à la hausse au prix de 4850.50

## Notes Importantes

- L'indicateur se réinitialise automatiquement chaque jour
- Les niveaux sont calculés en pourcentage du prix de référence
- Pour l'E-mini S&P 500 (ES), utilisez les paramètres par défaut (7%, 13%, 20%)
- Pour d'autres instruments, consultez les règles de limites du CME

## Référence

Basé sur les règles de limites de prix du CME Group :
https://www.cmegroup.com/trading/price-limits.html#equityIndex

## Version

- **PineScript** : Version 6
- **Type** : Overlay indicator
- **Compatibilité** : TradingView (tous les comptes)

## Licence

Libre d'utilisation et de modification
