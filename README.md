# Calibrated Alicante-Murcia Freeway SUMO Scenario

Contacts:  Juan Jesus Gonzalez [j.gonzalezd@umh.es], Javier Gozalvez [j.gozalvez@umh.es]

This scenario is designed for SUMO (Simulator of Urban MObility), version 0.32.0.


## Features

* Comprises 97 Km of freeway in the Mediterranean corridor.
* Include sections with two and three lanes, 36 on-ramps and 34 off-ramps.
* Approximate Average Daily Traffic (ADT) of 100.000 vehicles/day.
* Calibrated with Cadyts (1), using a novel methodology (2).
* Dataset composed of 9 days of measurements on 82 induction loops located in mainline lanes and on/off-ramps.
* Calibration of Light Vehicles and Heavy Vehicles.



## Files
Common files:
* `Alicante-Murcia_MW_LIMPIO_GR_CRECIENTE_beforeApril16.net.xml` SUMO road network file.
* `detectores_Ali-Mur_CREC_bAp16_Ord_567OK_best82_LIGEROS.xml` SUMO detector file for Light Vehicles.
* `detectores_Ali-Mur_CREC_bAp16_Ord_567OK_best82_PESADOS.xml` SUMO detector file for Heavy Vehicles.
* `detectores_Ali-Mur_CREC_bAp16_Ord_567OK_best82_MIX.xml` SUMO detector file for all vehicles.
* `rerouters.xml` SUMO additional file to include rerouters in the road network.
* `vtypes.xml` SUMO additional file to define vehicle types.

Each 12 hour period is calibrated independently, having its own demand file and configuration file:
* `altRoutesOutput_XXX.cal.xml` SUMO demand file.
* `iteration_XXX.sumocfg` SUMO configuration file.

## How To

The scenario is divided in 12 hour periods, each of which is calibrated independently, thus producing 18 different demand files for the 9 days dataset.

To run the scenario, place all the files above in the same directory (common files and corresponding 12 hour period files) and execute SUMO with the corresponding configuration file. For example:

```
sumo iteration_XXX.sumocfg
```

## References

(1) Cadyts – Calibration of Dynamic Traffic Simulations [https://people.kth.se/~gunnarfl/cadyts.html]

(2) Under development

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

This work was supported by the Spanish Dirección General de Tráfico (SPIP2017-02204).

