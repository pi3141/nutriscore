# nutriscore
compute nutriscore (2022 update) for main algorithm (not beverages nor oil)

[example : web page to compute nutriscore from recipe](https://pi3141.github.io/nutriscore.html)

## set up
source nutriscore.js in your html file :
 `<script src="nutriscore.js"></script>`
 
## usage
call compute_FNS function :
```
compute_FNS(energy, sugar, saturated_fats, salt, proteins, fibers, fruits_vegetables_percentage, red_meat, cheese)
```
 
The parameters are :
* energy in kJ / 100g
* sugar in g / 100g
* saturated_fats in g / 100g
* salt in g / 100g
* proteins in g / 100g
* fibers in g / 100g
* fruits_vegetables_percentage in masse percentage
* red_meat boolean
* cheese boolean

The function return a JS object containing the nutriscore class (letter from A to E), score (from −17 to 55), AScore, CScore and the contribution of each element to the nutriscore :
```
{
        FNS: {
            class,
            score,
            AScore,
            CScore
        },
        energy: {
            value: energy,
            score: 
        },
        sugar: {
            value: sugar,
            score: 
        },
        saturated_fats: {
            value: saturated_fats,
            score: 
        },
        salt: {
            value: salt,
            score: 
        },
        proteins: {
            value: proteins,
            score: 
        },
        fibers: {
            value: fibers,
            score: 
        },
        fruits_vegetables_percentage: {
            value: fruits_vegetables_percentage,
            score: 
        },
        red_meat: ,
        cheese: 
    }
```
