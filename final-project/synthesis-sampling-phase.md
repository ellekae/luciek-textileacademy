# sensor design + fabrication

### Nitrogen Dioxide

Nitrogen Dioxide \(NO2\) comes from a greater group of nitrogen oxides. It is an intermediate in the prouction of nitric acid, used to make fertilisers. It is found in the emissions of internal combustion engines burning fossil fuels, in vehicular emissions, gas stoves and cigarette smoke. 

Most atmospheric NO2 is emitted as NO, which is rapidly oxidized by ozone to NO2. NO2, in the presence of hydrocarbons and ultraviolet light, is the main source of tropospheric ozone and of nitrate aerosols, which form an important fraction of the ambient air PM2.5 mass. In addition, NO2 is responsible for what we call 'acid rain'.

NO2 is a product of combustion processes and is generally found in the atmosphere in close association with other primary pollutants, including ultrafine \(UF\) particles. It is itself toxic and is also a precursor of ozone, with which it coexists along with a number of other photochemically generated oxidants.

### Nitrogen Dioxide: Effects on human health

NO2 causes inflammation of the airways and it exacerbates asthmatic conditions significantly. 

Scientific evidence links short-term NO2 exposures, ranging from 30 minutes to 24 hours, with adverse respiratory effects including airway inflammation in healthy people and increased respiratory symptoms in people with asthma. Studies also show a connection between short-term exposure and increased emergency room visits and hospital admissions for respiratory illnesses.

Advised NO2 levels are designed to protect against exposure to the entire group of nitrogen oxides \(NOx\). NO2 is the component of greatest concern and is used as the indicator for the larger group of NOx. The sum of nitric oxide \(NO\) and NO2 is commonly called NOx. Other nitrogen oxides include nitrous acid and nitric acid. NOx reacts with volatile organic compounds to form ozone.

NO2 forms from ground-level emissions related to the burning of fossil fuels from vehicles, power plants, industrial sources, and off-road equipment, such as construction vehicles and lawn and garden equipment. In addition to contributing to ground-level ozone formation, NO2 is linked with a number of adverse effects on the respiratory system. NOx reacts with ammonia, moisture, and other compounds to form small particles. These small particles can penetrate deeply into sensitive parts of the lungs.

Unlike ozone and particle pollution, which can be of concern over large regions, NO2 levels are appreciably higher in close proximity to pollution sources \(e.g., vehicles on major freeways, factories\). Health effects associated with NO2 are much less likely farther away from these pollution sources. NO2 in heavy traffic or on freeways can be two times as high as levels measured in residential areas or on lesser traveled roads. Monitoring studies have shown that within approximately 50 meters of heavy traffic/ freeways, NO2 concentrations may be 30 to 100 percent higher.

This is significant given that information commonly available on NO2 is obtained via air monitoring stations situated around any given city. The NO2 concentrations of a particular area and personal NO2 exposure can represent two vastly different levels.  

### Nitrogen Dioxide as an ambient seam

Numerous epidemiological studies have used NO2 as a marker for the cocktail of combustion related pollutants, in particular, those emitted by road traffic or indoor combustion sources. In these studies, any observed health effects could also have been associated with other combustion products, such as ultrafine particles, nitrous oxide \(NO\), particulate matter or benzene.

Nitrogen dioxide \(NO2 \), for example, is a product of combustion processes and is generally found in the atmosphere in close association with other primary pollutants, including ultrafine \(UF\) particles. It is itself toxic and is also a precursor of ozone, with which it coexists along with a number of other photochemically generated oxidants. Concentrations of NO2 are often strongly correlated with those of other toxic pollutants, and being the easier to measure, is often used as a surrogate for the pollutant mixture as a whole. Achieving guideline concentrations for individual pollutants such as NO2 may therefore bring public health benefits that exceed those anticipated on the basis of estimates of a single pollutant’s toxicity.

sources: [https://www3.epa.gov/airnow/no2.pdf](https://www3.epa.gov/airnow/no2.pdf), [http://www.euro.who.int/\_\_data/assets/pdf\_file/0017/123083/AQG2ndEd\_7\_1nitrogendioxide.pdf](http://www.euro.who.int/__data/assets/pdf_file/0017/123083/AQG2ndEd_7_1nitrogendioxide.pdf), [https://apps.who.int/iris/bitstream/handle/10665/69477/WHO\_SDE\_PHE\_OEH\_06.02\_eng.pdf;sequence=1](https://apps.who.int/iris/bitstream/handle/10665/69477/WHO_SDE_PHE_OEH_06.02_eng.pdf;sequence=1)

### Converting values

The World Health Organisation \(WHO\) stipulates an limit of 200ug/m3 for NO2 exposure, after which point significant respiratory health impacts can be expected. This unit of measurement is not used often in the literature, and infact any research papers dealing with gas sensing and testing. 

To convert from ug/m3 to ppm we can use the following equation:

$$
ug/m3= ppm *molarVOL(NTP)
$$

We thus need to know the molecular weight of the target gas . - the molecular weight of NO2 is 46.01g/mol

From here we can calculate the molar volume of the target gas at normal temperature and pressure \(NTP\) or standard atmpospheric temperature and pressure \(SATP\)

$$
molar mass /density ofgas = molar volume
$$

or 

$$
ppb = (molL*ugm3)/gmol
$$

Therefore we can calculate the equivalent value in ppm for the WHO value of 200ug/m3 -- approximately 0.106 ppm. This is necessary for target gas testing. 

{% hint style="info" %}
To give some context, the average NO2 level for the area in which I live in HCMC is typically at 0.01ppm and I live in downtown HCMC which is generally understood to be quite polluted. We also know that the average NO2 readings in dense traffic are typically around the 0.5ppm level. 
{% endhint %}

Sensor response levels in the literature typically report a 6% response for 0.25ppm, a 12% response for 1.25ppm, and so on. 

### Reduced graphene oxide as a sensor

Reduced graphene oxide \(rGO\) can be used to detect NO2. This is possible as the NO2 molecule is an electron acceptor, therefore it strongly draws electrons from graphene. We thus find that in the presence of NO2 that the electrical conductivity of rGO will increase. 

rGO can be used as a sensor to detect other gases such as CO2, SO2, NH3, H2S and others, however the response for NO2 is an order of magnitude greater than that found with other gases. The only comparable response is for exposure to NH3, however their effects are entirely reversed: NO2 acts as a p-type dopant \(electron acceptor\) causing resistance in the sensor to drop, while NH2 acts as an n-type dopant \(electron donor\) causing resistance in the sensor to increase. The conductivity change in both cases is markedly different to other gases, and to one another.

source: Singh, Meyyappan et al. 2017. 'Flexible Graphene-Bsed Wearable Gas and Chemical Sensors' in Applied Materials and interfaces 2017, 9, 34544-34586. 

### Fabricating an rGO sensor on textile

There are numerous methods in the literature for reducing GO onto textile. I reviewed a selection protocols outlined in several research papers, then selected those with the potential to replicate in the context of a fab lab, or home studio as it were. I was able to test three prpotocols, the final being the most successful, as I will outline. 

I followed each protocol using GO that I purchased. Below I outline my reasoning behind the decision not to synthesize my own GO. 

{% hint style="danger" %}
Creating graphene oxide from graphite via [hummers](https://www.youtube.com/watch?v=aQcMYTiUPqA)/[tour ](https://www.youtube.com/watch?v=c17ePPuEaAk)method involves the use of extremely dangerous chemicals and an exothermic reaction which can result in serious injury in the unfortunate event that correct procedure is not followed. Three Chinese students were[ injured](https://www.shanghaidaily.com/metro/society/3-students-injured-after-blast-in-lab/shdaily.shtml) in a [blast](http://www.ecns.cn/2016/09-22/227472.shtml) that came from a lab involved in the synthesis of GO. Thus I would advise against synthesising GO within the context of fab labs/textile academy -- imo DIY GO is NOT OK.
{% endhint %}

At my home studio, I followed three distinct methods to create an rGO soft sensor:

1. Repeated dip coat and heat press method \(thermal reduction\)
2. Single dip coat method using poly-styrenesulfonate \(PSS\) as binding agent and sodium hydrosulphite \(Na2S2O4\) as reducing agent \(chemical reduction\)
3. Three step dip coating method \(chemical reduction\)

#### Dip coat and heat press \(Method 1\)

* prepare GO dispersion in DI water at 5mg/mL concentration
* deposit onto textile using [vaccuum filtration](https://duckduckgo.com/?q=vaccuum+filtration+graphene&atb=v1-1&ia=videos&iax=videos&iai=dQC23DWHxMA&pn=1) \(set up [here](https://duckduckgo.com/?q=vaccuum+filtration+graphene&atb=v1-1&ia=videos&iax=videos&iai=Oy2v40jOLYo&pn=1)\)
* heat press at 180 degrees C for 30 minutes \(thermal reduction temperature should be over 200 degrees however to avoid damaging cotton fibres was reduced to a level at which reduction would still occur whilst preserving the textile\)

source: Ren, Wang et al. 2016. 'Environmentally-friendly conductive cotton fabric as flexible strain sensor based on hot press reduced graphene oxide' in Carbon 111 \(2017\) 622-630. 

#### Single dip coat method \(Method 2\) 

* prepare GO dispersion in DI at 1mg/mL concentration
* add 1.6g PSS and stir vigorously, transfer to a flask
* add 1.2g Na2S2O4 and NH3 to adjust pH to 9-10, stir vigorously
* hold mixture at 90 degrees C for 12 hours
* rinse mixutre with DI water to retain rGO yet remove excess chemicals
*  dip textile/thread in rGO mixture and dry at 100 degrees C for 10 minutes. repeat up to 10 times. 

source: Karim, N., Afroj, S., Tan, S., He, P., Fernando, A., Carr, C., & Novoselov, K. \(2017\). Scalable Production of Graphene-Based Wearable E-Textiles. ACS Nano, 11\(12\), 12266-12275.

#### Three step dip coating method \(Method 3\)

* prepare aqueous dispersion of GO in DI water at 0.05%
* soak textile in GO solution for 30 minutes at room temperature
* dry at 90 degrees for 30 mins
* repeat 3 times
* immerse GO coated sample in 100mL aqueous solution of 25mM Na2S2O4. maintain at 95 degrees for 60 minutes, with stirring
* wash carefully
* dry at 90 degrees for 30 minutes

source: Shateri-Khalilabad and Yazdanshenas. 2013. 'Fabricating electroconductive cotton textiles using graphene' in Carbohydrate Polymers 96 \(2013\) 190-195.

### Analysis of Protocols

Due to limitations in terms of equipment and resources, I believe that my success in achieving stable results was impacted to some degree. I was able to obtain sensors on cotton and poly-cotton for both methods 2 and 3, however only poly-cotton sensors prepared by method 3 were stable enough to be included in a circuit. 

The successfully prepared sensors are electrically conductive with high resistance -- 19,500 Ohms at standard air temperature and pressure \(SATP\). 



I tested the sensor by connecting it via an Arduino UNO to an LCD and compared it to known resistance value of 16,600 Ohms. For comparison, I used a handheld NO2 sensor. I held the sensor directly in front of motorbike exhaust and found that at 7ppm the resistance dropped to around 13,000 Ohms. I also found that it took the sensor up to an hour to recover sensitivity, despite exposure to strong natural UV light \(UV index 12\) and having removed the NO2 exposure. 

#### Future Work

I intend to follow this work up with the fabrication of silk based rGO sensors using alternative binding agents to see if they are more stable/less fragile. I would also like to code the Uno and Nano to reflect the recovery time of the sensor such that when the threshold NO2 level a significant delay is instigated before beginning to check resistance levels again. 

