# Timeline & File Naming Convention

```{attention}
Ready to make your model outputs accessible to other MIP participants? Please refer to [this page](https://arm-development.github.io/comble-mip/CONTRIBUTING.html) to learn how to upload your model outputs to the repository.
```

Processed model outputs are invited for commit to the GitHub repository under **/comble-mip/output_xxx/YOUR_MODEL_NAME/** where *xxx* can be *les* or *scm*. Within your model's subdirectory, you should place any intermediate or sensitivity simulations in a directory called **devel**. Once you are happy with your simulations for the specifications outlined in the tables below, you may host them in a directory called **sandbox**. While these can be committed and removed at any time, note that we expect **sandbox** simulations to be finalized by the dates listed below.

We request that you name your simulations as outlined below so that they can be readily compared with other runs using the same test specification. Please add a prefix to each of the file names to distinguish between other models. For example, for the *SCM, liquid-only* specification in Part I, outputs from the ModelE3 SCM model should be named ***ModelE3_FixN_noice***. If your submission is for an LES model, then we ask that you also include a prefix indicating the domain size (units of km) and grid cell spacing (units of m). For example, for the *Small-domain LES, liquid-only* specification in Part I, outputs from the DHARMA LES model should be named ***DHARMA_Lx25_dx100_FixN_noice***.

Our requested prefixes for the domain size and grid cell spacing are as follows for the LES runs:
* Small-domain (Lx=25.6 km, dx=100 m): ***Lx25_dx100***
* Large-domain (Lx=128 km, dx=100 m): ***Lx125_dx100***

If you have additional LES submissions that have different domain sizes and/or grid cell spacings, then we ask that you adjust your prefix information accordingly. 

## Part 1
| Product                                                                                                                                                      | Simulation Name                                                                        | Request Date                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| SCM/Small-domain LES, liquid-only<br>SCM/Small-domain LES with ice<br>SCM/Small-domain LES with ice, default roughness lengths*<br>Large-domain LES with ice | *{prefix}*_FixN_noice<br>*{prefix}*_FixN<br>*{prefix}*_FixN_def_z0<br>*{prefix}*_FixN | Mar. 1, 2024<br>Mar. 1, 2024<br>Mar. 1, 2024<br><span style="color:red">**TBD**</span>** |

## Part II
| Product                                                                                                                                                      | Simulation Name                                                  | Request Date                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------|
| SCM/Small-domain LES, prognostic aerosol, diagnostic ice<br>SCM/Small-domain LES, prognostic aerosol and ice<br>Large-domain LES, prognostic aerosol and ice | *{prefix}*_ProgNa<br>*{prefix}*_ProgNaNi<br>*{prefix}*_ProgNaNi | Apr. 1, 2024<br>Apr. 1, 2024<br><span style="color:red">**TBD**</span>** |

## Part II (optional; all SCM/small-domain LES)
| Product                                                                                                                      | Simulation Name                                                                                | Request Date                                                     |
|------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| Prognostic droplet, no ice<br>Prognostic droplet, diagnostic ice<br>Prognostic droplet and ice<br>Prognostic aerosol, no ice | *{prefix}*_ProgNc_noice<br>*{prefix}*_ProgNc<br>*{prefix}*_ProgNcNi<br>*{prefix}*_ProgNa_noice | <span style="color:red">**TBD**</span>^<br><span style="color:red">**TBD**</span>^<br><span style="color:red">**TBD**</span>^<br><span style="color:red">**TBD**</span>^ |

## Notes
*This simulation will use the default roughness length formulations in each host model. All other simulations will use the fixed roughness lengths as defined on the [Main Model Configuration page](https://arm-development.github.io/comble-mip/main_configuration.html).
<br>
**Given its high computational cost, we suggest that participants refrain from running this setup in case there are any last minute tweaks to the model forcing; for instance, large-scale forcing required to generate realistic roll structures.
<br>
^We plan to first evaluate model outputs before recommending a request date for these additional sensitivity simulations.
