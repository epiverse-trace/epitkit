---
title: Glossary
editor_options: 
  markdown: 
    wrap: 72
---

# Epidemic Theory and Models

## Mathematical Model of Infectious Diseases

A mathematical model in the epidemic theory of infectious diseases is an abstract representation that uses mathematical equations and algorithms to describe the dynamics of infection spread within a population. These models allow for understanding, predicting, or projecting how an infectious disease can spread and affect a community, considering various factors such as the transmission rate, infectious period, recovery, and immunity.

The classic mathematical model is the SIR model: Susceptible, Infectious, and Recovered. This traditionally uses ordinary differential equations (ODEs).

There are several types of mathematical models, the most common being: [deterministic](#deterministic-model) and [stochastic](#stochastic-model).

## Ordinary Differential Equations (ODEs)

Ordinary differential equations (ODEs) can be used to represent the rate of change of one variable (e.g., the number of infected individuals) with respect to another (e.g., time). ODEs are widely used in infectious disease modeling to model the flow of individuals between different disease states.

For more information, consult this introduction to [ODEs](https://mathinsight.org/ordinary_differential_equation_introduction).

## Deterministic Model

A deterministic model is a type of mathematical model in which the behavior of the system is completely determined by its initial conditions and model parameters, without involving elements of randomness or uncertainty. In other words, given a set of initial conditions and parameters, the model will always produce the same results.

## Stochastic Model

A stochastic model addresses the random variation of parameters in model simulations for the same initial conditions. This means that the exact same results will not always be obtained in all simulations. Examples include stochastic differential equations and branching process models. For more details, consult [Allen (2017)](https://www.sciencedirect.com/science/article/pii/S2468042716300495?via%3Dihub).

## Initial Conditions

In Ordinary Differential Equations (ODEs), initial conditions are the values of each compartment at the initial time of the model (time zero). These conditions are necessary to start the simulation of the epidemic in the model and can significantly affect subsequent results.

Example: If there is one infectious individual in a population of 1000 in a Susceptible-Infectious-Recovered model, the initial conditions would be:
* $S_0=999$
* $I_0=1$
* $R_0=0$

## Transmission Model Parameters

Model parameters are values that allow the movement of individuals between different compartments; they describe the flow between disease states. These include, for example: the recovery rate which is a model parameter that can be used to describe the flow between infectious and recovered states.

## State Variables

State variables in a model represented by ordinary differential equations are the disease states in which individuals can be. For example, if individuals can be susceptible, infectious, or recovered, the state variables are S, I, and R. There is an ordinary differential equation for each state variable.

## Susceptible

Population with no prior or current exposure to the pathogen, or without vaccination, and therefore having neither infection nor humoral immune protection (neutralizing antibodies) against the pathogen. (Related to state variables)

Examples:
* In 2020, at the beginning of the COVID-19 pandemic, the entire world population was considered susceptible.
* Children not vaccinated against measles and who have not been infected or have not developed post-infection antibodies.

## Infectious

Population with active presence of the pathogen capable of transmitting it to susceptible individuals in the population. This state has a duration equivalent to the infectious period.

Example:
* Patient living with HIV not receiving antiretroviral treatment with a high viral load who has unprotected sex.

## Recovered

Population with neutralizing antibodies against the pathogen. This immunity could have been acquired via natural infection or vaccination. This state has a duration equivalent to the period of neutralizing immunity duration. (Related to state variables)

Example:
* Person vaccinated against yellow fever. This vaccine provides high, long-lasting protection against the infection.

## Exposed

Population that has been infected with a pathogen but is not yet capable of transmitting the infection (infected, but not infectious). This state has a duration equivalent to the latency period.

Example:
* The transmission of the tuberculosis bacillus occurs from positive bacilliferous subjects who release bacilli into the environment, and exposed individuals are easily infected. However, for many years individuals can remain infected but controlling the disease, without transmitting it; these individuals are considered exposed in dynamic transmission models.

## Spillover

In epidemiology, the term spillover refers to the process by which a pathogen (microorganism, whether virus, bacterium, parasite, or other), which normally affects a specific animal species, is transmitted to another reservoir. In other words, it is the evolutionary leap of a pathogen between species, which includes transmission from an animal to a human.

## Zoonosis

PAHO defines zoonosis as "infectious diseases naturally transmissible from vertebrate animals to humans".

## Transmission Parameters

## Basic Reproduction Number, $R_0$

It is defined as the average number of secondary cases produced from a primary case in a totally susceptible population, i.e., at time 0. This number is specific to each infectious agent, although it can also be affected by climatic and social variables, and represents the transmission potential of the pathogen. This value is theoretical and also determines the herd immunity threshold. It is a measure of the transmissibility of an infection. It is calculated as:

$R_0 = p * c * D$

Where,
$p$ = probability of infection after contact
$c$ = contact rate
$D$ = duration of the infectious period

Example:
* The following diagram compares the $R_0$ of seasonal influenza, Ebola, Diphtheria, Smallpox, and Measles respiratory syndrome.

## Effective Reproduction Number, $R_t$

It is defined as the average number of secondary cases from an infectious case in the population composed of susceptible and non-susceptible hosts per unit of time (t). It is calculated as:

$R_t = R_0 * S$

Where:
$R_0$ = Basic reproduction number
$S$ = proportion of susceptibles in the population

Characteristics of the Effective Reproduction Number, $R_t$:
* **Temporal:** $R_t$ reflects the current situation of disease transmission and changes over time.
* **Contextual:** Unlike $R_0$, which assumes a completely susceptible population, $R_t$ considers the impact of acquired immunity (by infection or vaccination) and public health interventions (such as social distancing, quarantines, and mask use).

Interpretation:
* $R_t > 1$: The infection is spreading in the population.
* $R_t = 1$: The infection remains stable in the population.
* $R_t < 1$: The infection is decreasing and may eventually disappear.

$R_t$ can be influenced by two large groups of factors:
* Control measures: antimicrobial drugs, barrier measures (condoms, masks), and contact reduction measures (isolation, distancing, use of mosquito nets, fumigation, etc.)
* Acquisition of immunity through neutralizing antibodies (reduction of susceptibles as an epidemic progresses or vaccination).

## Contact Rate

The **contact rate** is an epidemiological measure that describes the frequency with which individuals in a population come into contact with each other, within a specific time period, in a way that allows for the possibility of infectious disease transmission. This rate is fundamental to understanding and modeling the dynamics of disease spread within a community.

Characteristics of the Contact Rate:
* **Frequency:** Reflects the number of potentially infectious contacts per individual in a given time period.
* **Homogeneous vs. Heterogeneous:** The contact rate can be homogeneous, if contacts are distributed uniformly among all individuals, or heterogeneous, if some individuals have more contacts than others, which is common in reality.
* **Influence of Factors:** The rate can vary depending on factors such as age, behavior, environment, and control measures (e.g., social distancing).

Calculation of the Contact Rate: The contact rate can be estimated from empirical data collected through surveys, observational studies, or inferences from mathematical models.

## Contact Matrix

A **contact matrix** is an epidemiological tool that represents the contact rates between different groups in a population, normally organized by categories such as age, gender, or geographical location. Each element in the matrix indicates the frequency with which individuals from a specific group have contact with individuals from another group.

Characteristics of the Contact Matrix:
* **Structure:** It is a square matrix, where rows and columns represent the different population groups.
* **Elements:** Each cell of the matrix shows the average number of contacts between individuals of the corresponding groups.
* **Data:** Data can be collected through surveys, observational studies, or inferred from mathematical models.

## Latency Period

Time interval between exposure to an infectious agent with successful transmission and the onset of the infectious period. During the latency period, infected individuals do not transmit the infection.

Examples:
* For tuberculosis, the latency period is usually prolonged, and after contagion, individuals remain without transmitting the disease for many years.
* For SARS-CoV-2 infection, the latency period was short (2-4 days) and also shorter than the incubation period, so individuals could transmit the infection before the onset of symptoms.

## Incubation Period

Time interval between exposure to an infectious agent with successful transmission and the onset of clinical disease (signs and symptoms). For diseases where the onset of the infectious period coincides with the appearance of signs and symptoms, the latency and incubation periods are the same.

Example:
* In the study by Wu et al. 2022, a systematic review of the incubation periods of SARS-CoV2 was conducted. It was found that: the average incubation period of COVID-19 was 5.00 days (95% CI, 4.94-5.06 days) for cases caused by the Alpha variant, 4.50 days (95% CI, 1.83-7.17 days) for the Beta variant, 4.41 days (95% CI, 3.76-5.05 days) for the Delta variant, and 3.42 days (95% CI, 2.88-3.96 days) for the Omicron variant. The findings of this study suggest that SARS-CoV-2 has continuously evolved and mutated throughout the COVID-19 pandemic, producing variants with different levels of transmission and virulence. Identifying the incubation period of the different variants is a key factor in determining the isolation period.

## Infectious Period

Time interval during which the infected individual has active pathogen replication and can transmit it to other individuals. Since this period can overlap with the incubation period, it can be difficult to obtain accurate estimates of the infectious period. Viral load and detection of infectious virus are the two key parameters for estimating infectivity ([Puhach et al., 2022](https://www.nature.com/articles/s41579-022-00822-w) and [Hakki et al, 2022](https://www.thelancet.com/journals/lanres/article/PIIS2213-2600(22)00226-0/fulltext)).

Example:
* In cases of respiratory viruses (e.g., influenza, SARS-CoV-2) this period can last days, while for diseases like HIV or tuberculosis it can last years.

## Recovery Time

Time interval between the onset of the infectious period and the moment an individual stops transmitting the pathogen.

Example:
* In cases of chickenpox, subjects stop transmitting the pathogen when all lesions have crusted over. Therefore, the recovery period appears before the disappearance of the lesions. After this period, subjects are considered recovered.

## Generation Time

Time interval between the onset of the infectious period of a primary case and the onset of the infectious period in a secondary case, infected by the primary case. It is normally unknown and is approximated by the serial interval. It cannot be measured, only estimated.

Example:
* The study by Hart et al. 2022 in the United Kingdom between February and August 2021 recruited 227 households with 559 participants. It was found that the Delta variant transmitted faster than the Alpha variant in households, with a shorter mean generation time: 4.7 days for Delta versus 5.5 days for Alpha. This suggests that Delta spreads more rapidly in households due to a rapid decrease in susceptible individuals, which could make interventions such as contact tracing and isolation less effective.

## Serial Interval

Time period between the **onset of symptoms** of a primary case and the onset of symptoms in a secondary case infected by the primary case. It is measurable given that data such as dates of symptom onset can be obtained. This value can be negative when presymptomatic infection occurs. The distribution of the serial interval of an infection is commonly used to estimate the distribution of the generation time ([Cori et al., 2017](https://royalsocietypublishing.org/doi/10.1098/rstb.2016.0371)). The relationship between the serial interval and the incubation period helps define the type of infection transmission (symptomatic or presymptomatic) ([Nishiura et al., 2020](https://www.ijidonline.com/article/S1201-9712(20)30119-3/fulltext#gr2)).

Example: In the study by Nishiura et al. 2020, the serial interval of COVID-19 was estimated from 28 infector-infected pairs. The onset dates of disease for primary and secondary cases were analyzed, adjusting for right truncation because the epidemic was still growing. The results showed that the median serial interval was 4.0 days in the full dataset and 4.6 days in the subset of pairs with greater certainty. It is concluded that the serial interval of COVID-19 is close to or shorter than its incubation period, suggesting significant transmission before symptom onset, and is shorter than the serial interval of SARS, which could introduce bias in calculations based on SARS.

## Attack Rate

The **attack rate** is an epidemiological measure that describes the proportion of people in a specific population who develop a disease or infection during a defined period, generally in the context of an outbreak or epidemic. This rate includes both disease cases and asymptomatic infections, and may require seroprevalence studies or mathematical models for accurate calculation.

Characteristics:
* **Purpose:** Evaluates the proportion of people who become ill or infected among those initially exposed.
* **Context:** Used to measure the immediate impact of exposure to an infectious agent.

## Symptomatic Secondary Attack Rate

The **symptomatic attack rate** measures the proportion of exposed people who develop clinical symptoms of the disease. It focuses exclusively on those individuals who present symptoms, thus differentiating itself from the general attack rate which may include asymptomatic cases.

Characteristics:
* **Purpose:** Evaluates the proportion of exposed people who develop clinical symptoms, providing a measure of the clinical manifestation of the disease.
* **Context:** Used to understand the severity and clinical impact of the disease in a specific population.

## Secondary Attack Rate (SAR)

The **secondary attack rate** measures the proportion of cases that occur among close contacts of primary cases. It focuses on the secondary transmission of the disease, that is, the spread of the disease from initial cases to other individuals in close contact.

Characteristics:
* **Purpose:** Measures the transmission of the disease among close contacts of primary cases.
* **Context:** Used to evaluate the effectiveness of control measures and to better understand the dynamics of disease transmission.

## Herd Immunity Threshold

The **herd immunity threshold** is the proportion of the population that must be immune to an infectious disease, either through vaccination or previous infection, for the spread of the disease to decrease and eventually stop. When this threshold is reached, even non-immune individuals are indirectly protected due to the reduced probability of pathogen transmission.

Characteristics of the Herd Immunity Threshold:
* **Critical Proportion:** Represents the fraction of the population that needs to be immune to interrupt sustained transmission of the infection.
* **Dependence on R₀:** The threshold is directly related to the basic reproduction number ($R_0$) of the infection, which is the average number of secondary cases produced by a primary case in a completely susceptible population.

Calculation: The herd immunity threshold depends on the basic reproduction number $R_0$ and is defined as $1 - \frac{1}{R_0}$. The more contagious a pathogen is, the higher its $R_0$ and the greater the proportion of the population that must be immune to block sustained transmission.

Example:
* In the case of measles, for an $R_0$ of 18, herd immunity is approximately 95%.

## "Overshoot"

The term **overshoot** refers to the phenomenon in which the number of cases of an infectious disease exceeds the herd immunity threshold during an outbreak or epidemic, before disease transmission decreases and stabilizes. This excess of cases occurs despite a sufficient proportion of the population having achieved the necessary immunity to slow the spread of the disease.

Characteristics of Overshoot:
* **Excess Cases:** Occurs when there are more cases than expected even after reaching the herd immunity threshold.
* **Temporal:** It is a transient phenomenon observed before the disease stabilizes or disappears.
* **Herd Immunity:** Indicates that the herd immunity threshold has been reached but transmission initially continues due to epidemic dynamics.

Causes of Overshoot:
* **Epidemic Inertia:** The disease continues to spread due to the number of susceptible individuals still exposed to the infectious agent before transmission is reduced.
* **Heterogeneous Immunity Distribution:** Immunity is not uniformly distributed in the population, allowing localized outbreaks to occur.

## Critical Community Size (CCS)

It is the minimum size of a closed population required for an infectious agent to persist in that population. If the population number is too low, after an outbreak the pathogen cannot persist and disappears. This critical mass of susceptibles is determined by the characteristics of the agent, the demographic structure, and the hygienic conditions of the host population.

Example: For measles, which has a high $R_0$, the CCS is relatively large. Studies have shown that measles needs a population of at least 250,000 to 500,000 individuals to remain endemic. In contrast, diseases with a lower $R_0$ may have a much smaller CCS.

## Superspreading

**Superspreading** is a phenomenon in the epidemiology of infectious diseases where a small number of infected individuals are responsible for a large proportion of new infections. These individuals, known as "superspreaders," infect a much larger number of people than the expected average, thus accelerating the spread of the disease.

Characteristics of Superspreading:
* **Variability in Transmission:** There is great heterogeneity in the ability of individuals to transmit the disease, with a few individuals causing many infections while most cause few or none.
* **Dispersion Factor (k):** The degree of superspreading can be quantified using the parameter k. Low k values indicate high superspreading, while values close to 1 indicate that the dispersion is more uniform.
* **Specific Context:** Superspreading events usually occur in specific contexts such as mass gatherings, confined spaces, and activities where there is prolonged close contact.

Example: During the COVID-19 pandemic, several superspreading events were observed, such as a single infected person infecting dozens of people at a religious gathering in South Korea. In another case, a choir event in the United States resulted in many infections from a single infected individual.

Example:
* In South Korea during the COVID-19 pandemic, superspreading events occurred in the context of religious choirs, with 11 transmission clusters associated with 641 COVID-19 disease cases.

## Exponential Growth Rate

The **exponential growth rate** is an epidemiological measure that describes the speed at which the number of cases of an infectious disease increases in a population at the initial time of an epidemic, when control measures have not been implemented or are minimal. This rate is fundamental for understanding the dynamics of disease spread in its early stages and for planning public health interventions.

Calculation of the Exponential Growth Rate: The exponential growth rate can be calculated using the formula:

$$r = \frac{\ln(C_t) - \ln(C_0)}{t}$$

Where:
* $r$ is the exponential growth rate.
* $C_t$ is the number of cases at time t.
* $C_0$ is the initial number of cases.
* $t$ is the elapsed time.

## Severity Parameters

## Lethality

Refers to the severity of the disease with respect to death. This can be classified as IFR or CFR.

## Infection Fatality Ratio (IFR)

Probability of death after infection (symptomatic or asymptomatic).

Example:
* For SARS-CoV-2, age is by far the main risk factor for death. Therefore, the average IFR of a population depends on its demographic structure.

## Case Fatality Ratio (CFR)

Probability of death among reported cases. It generally only includes symptomatic cases confirmed by laboratory or by clinic. Therefore, the CFR will always be higher than the IFR.

Example:
* The reported CFR for Ebola has been estimated in different outbreaks between 30-70%.

## Hospitalization Fatality Ratio (HFR)

The **Hospitalization Fatality Ratio (HFR)** is an epidemiological parameter that measures the proportion of hospitalized individuals with a specific disease who die from that disease. This ratio is a measure of the severity of the disease among those requiring hospitalization and provides crucial information about the effectiveness of hospital treatment and the severity of the disease in the most severe cases.

## Biases in Parameter Reporting

## Phase Bias (Dynamic or Epidemic)

Considers the susceptibility of the population at the times when transmission pairs (cases and contacts) are observed. It is a type of sampling bias. It affects retrospective data and is related to the phase of the epidemic: during the exponential growth phase, recently symptomatic cases are overrepresented in the observed data, while during the decline phase, these cases are underrepresented, leading to the estimation of shorter and longer delay intervals, respectively ([Park et al., in progress](https://github.com/parksw3/epidist-paper)).

## Reporting Delay

Delay or lag between the time an event occurs (e.g., symptom onset) and the time it is reported ([Lawless, 1994](https://www.jstor.org/stable/3315820)). We can quantify it by comparing the case list with successive versions of the same or with updated aggregated reported case counts ([Cori et al., 2017](https://royalsocietypublishing.org/doi/10.1098/rstb.2016.0371)).

## Right Truncation Bias

A type of sampling bias related to the data collection process. It arises because only cases that have been reported can be observed. Failure to account for right truncation during the growth phase of an epidemic can lead to an underestimation of the average delay ([Park et al., in progress](https://github.com/parksw3/epidist-paper)).

## Censoring

Means that we know an event occurred, but we don't know exactly when it occurred. Most epidemiological data are "doubly censored" because there is uncertainty in both primary and secondary event times. Failure to account for censoring can lead to biased estimates of the standard deviation of the delay ([Park et al., in progress](https://github.com/parksw3/epidist-paper)). Different sampling approaches can generate biases due to left and right censoring in serial interval estimation, which can propagate bias to the estimation of the incubation period and generation time ([Chen et al., 2022](https://www.nature.com/articles/s41467-022-35496-8/figures/2)).

## Relative Risks

## Risk Ratio (RR)

The Risk Ratio (RR), also called Relative Risk, compares the risk of developing a health event (disease, death) between two groups. It does so by dividing the risk (incidence proportion, attack rate) in group 1 by the risk (incidence proportion, attack rate) in group 2. The two groups are generally differentiated by demographic factors such as sex or by exposure to a suspected risk factor, for example, food consumption or contact with suspected cases.

The formula for the Risk Ratio (RR) is:

Risk of disease (incidence proportion, attack rate) in the primary group of interest / Risk of disease (incidence proportion, attack rate) in the comparison group

From this, it can be concluded that:
* If RR is equal to 1, it indicates an identical risk between the two groups.
* If RR is greater than 1, it indicates a higher risk for the numerator group, generally the exposed group.
* If RR is less than 1, it indicates a decreased risk for the exposed group, which suggests that the exposure may actually protect against the onset of disease.

Example:
* In an outbreak of a respiratory virus among school students, 28 out of 157 elementary school students developed tuberculosis, compared to 4 out of 137 high school students. Defining exposure as being an elementary school student, and non-exposure as being a high school student, we have:

| | Sick | Healthy | Total |
|---|---|---|---|
| **Elementary students** | 30 | 120 | 150 |
| **High school students** | 5 | 135 | 140 |
| Total | 35 | 265 | 290 |

To calculate RR, first calculate the attack rate for each group:
Attack rate for exposed (Tuberculosis Primary School) = $\frac{30}{150} = 0.2 = 20\%$
Attack rate for non-exposed (Tuberculosis Secondary School) = $\frac{5}{140} = 0.036 = 3.6\%$

Thus, the RR is simply the ratio of these two risks:
$RR = \frac{20}{3.6} = 5.5$

Therefore, elementary school students were 5.5 times more likely to develop tuberculosis compared to high school students.

## Odds Ratio (OR)

In case-control studies, the **Odds Ratio (OR)** is used to compare the odds of exposure to a risk factor between cases (individuals with the disease) and controls (individuals without the disease). This measure helps evaluate the association between exposure and disease.

Odds of exposure among cases / Odds of exposure among controls

It is important to note that the result is not a probability.

Furthermore, if this number is:
* Equal to 1, it means that the frequency of the event is equal in exposed and non-exposed, meaning there is no association between exposure and the event.
* Greater than 1, it means that the frequency of the event is higher in exposed than in non-exposed, which means that exposure is a risk factor.
* Less than 1, it means that the frequency of the event is lower in exposed than in non-exposed, and in this case, it is interpreted as the exposure being a protective factor.

Example:
After an Academic Conference, an outbreak of vomiting and diarrhea was reported after lunch. Lunch included sandwiches. The total attendance was 100 people; of whom 50 attendees became ill. During the initial investigation, it was found that a total of 60 people reported having eaten the lunch sandwich. Of these 60, 35 became ill, and of the 40 who did not eat the sandwich, 15 reported symptoms of illness. Summarizing:

| | Sick (Cases) | Healthy (Controls) | Total |
|---|---|---|---|
| **Exposed (Ate Sandwich)** | 35 | 25 | 60 |
| **Non-exposed (Did Not Eat Sandwich)** | 15 | 25 | 40 |
| Total | 50 | 50 | 100 |

Calculating, we have that:
Odds of exposure in cases: $\frac{35}{15} = 2.33$
Odds of exposure in controls: $\frac{25}{25} = 1$
Odds Ratio of exposure (OR) $= \frac{2.33}{1} = 2.33$

This means that the odds of presenting the reported symptoms of illness due to exposure to sandwich consumption are 2.33 times the odds of developing these symptoms without having consumed the sandwich. This can be interpreted as having eaten the sandwich being a risk factor.

## Outbreak Investigation

## Epidemic Curve

The **epidemic curve** is a graphical representation that shows the distribution of disease cases over time during an outbreak or epidemic. It is a fundamental tool in epidemiology to understand the dynamics of an epidemic, identify its origin, evaluate the effectiveness of interventions, and predict its evolution.

Characteristics of the Epidemic Curve:
* **X-axis (Horizontal):** Represents time (days, weeks, months, etc.).
* **Y-axis (Vertical):** Represents the number of new disease cases in each unit of time.
* **Patterns:** The shape of the curve can vary depending on how the disease is transmitted and the characteristics of the outbreak.

Types of Epidemic Curves:
1.  **Point Source Curve (or Common Source Exposure):**
    * **Characteristics:** Has a sharp peak followed by a rapid decline. It usually occurs when all cases are exposed to a common source of infection at a single moment or within a short period of time.
    * **Example:** A food poisoning outbreak at a social event where all cases are exposed to contaminated food at the same time.
2.  **Persistent Common Source Curve:**
    * **Characteristics:** The curve shows a prolonged plateau followed by a drop, indicating continuous or intermittent exposure to a common source of infection.
    * **Example:** A cholera outbreak in a community due to contaminated water supply that is not immediately corrected.
3.  **Person-to-Person Transmission Curve:**
    * **Characteristics:** Shows multiple successive peaks, reflecting the transmission of the disease from one person to another. Each peak represents a new generation of cases.
    * **Example:** A seasonal flu outbreak, where the first case infects others, who in turn infect more people, creating several peaks over time.

## Endemicity

Implies relatively stable levels of transmission reflected in a more or less constant incidence of cases. This does not mean that there are no sudden changes in incidence, with periods of high transmission, due, for example, to seasonal phenomena or sudden changes in the number of susceptibles (immigrants, for example). The boundary between endemicity and epidemicity is very difficult to establish, with the exception of imported diseases, where the previous endemic level was zero. Endemics can experience temporary changes in their manifestation, which can be described as cycles.

## Epidemicity

Implies instability in transmission, changing levels that can range from zero to millions of cases.

## Outbreak

A term commonly used to describe the sudden and unexpected appearance of cases of a disease.

## Seasonal Cycles

Occur linked to seasons (winter and respiratory viruses in temperate countries), or to climatic cycles (rainy season and malaria in the tropics).

## Pandemic

Refers to epidemics of great magnitude in terms of geographical extent and prolonged duration, such as influenza, cholera, or AIDS in our time.

## Basic Concepts

## Infection vs. Disease

Infection is the process in which an infectious agent enters, develops, and multiplies in the organism of a person or animal. During infection, an individual can be infectious, meaning capable of transmitting the agent to others, even if they do not present symptoms.

Disease, on the other hand, is the state in which an infection results in the development of clinical symptoms. An individual with disease is generally infectious, but there may be periods when they are infectious before showing symptoms.

Example: A person can be infected with the HIV virus and be infectious without showing symptoms for years. However, when they develop AIDS, they present severe symptoms. It is crucial to understand that the infectious agent (like HIV) is transmitted, not the symptoms of the disease (like AIDS).

This distinction is very important in the epidemiology of infectious diseases.

## Pathogen

A **pathogen** is a microorganism that can cause disease in a host organism. These can be subdivided into living and non-living. Living ones include bacteria, such as *Mycobacterium tuberculosis* which causes tuberculosis; parasites, such as *Plasmodium falciparum* which causes malaria; and fungi, such as *Candida albicans* which causes candidiasis. Although viruses, such as SARS-CoV-2 which causes COVID-19, are also pathogens, they are not considered living because they cannot carry out metabolic processes by themselves and require a host cell to replicate. All these pathogens invade, replicate, and damage host tissues, causing diseases. Their study is fundamental in epidemiology to develop effective strategies for the prevention, control, and treatment of infectious diseases.

## Case

A **case** is a person identified as suffering from a disease or event of epidemiological interest, either through clinical diagnosis, laboratory tests, or epidemiological criteria. Cases can be classified as follows:
* **Suspected case:** Individual who presents symptoms compatible with a disease but has not yet been confirmed by laboratory tests.
* **Probable case:** Individual who shows signs and symptoms of a disease and meets specific epidemiological criteria, but lacks laboratory confirmation.
* **Confirmed case:** Individual diagnosed with a disease through specific laboratory tests.
* **Index case (primary case):** The first case detected or reported in an epidemic outbreak.
* **Secondary case:** A case that occurs as a result of transmission from the index or primary case.

## Host

A living person or animal (mammal, reptile, bird, etc.), which under natural circumstances allows the subsistence or lodging of an infectious agent. Arthropod insects are not considered hosts.

## Vector

A vector can be defined as a living organism capable of transmitting an infectious agent between other living organisms ([WHO, 2020](https://www.who.int/news-room/fact-sheets/detail/vector-borne-diseases)). However, this definition may vary according to the criteria used. Some of the criteria used include the anthropocentric approach (diseases transmitted to humans), the micropredator approach (which emphasizes the ingestion of host fluids through direct contact), the hematophagous arthropod approach (arthropods that feed on blood), the morbidity-based approach (transmission of diseases to the host), the mobility-based approach (vector with high mobility), and the sequential infection transmission approach (mutual transmission of infection between vector and host) ([Wilson et al., 2017](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5352812/#RSTB20160085C19)). Depending on the selected points, the definition can vary and encompass diverse living beings. In addition, transmission can be a simple mechanical carrying function (Mechanical Transmission), or the infectious agent can multiply or develop within the vector (Biological Transmission).

Example: The *Aedes aegypti* mosquito is a vector of the Dengue virus.

## Carrier

A person (or animal) that harbors a specific infectious agent without presenting clinical symptoms or signs of it, and that constitutes a potential source of infection for humans.

## Reservoir

Any human, animal, arthropod, plant, soil, or inanimate matter, or combination thereof, where an infectious agent normally lives and multiplies and from which it depends for its survival, reproducing in such a way that it can be transmitted to a susceptible host.

## Minimum Community Size (MCS)

It is defined as the minimum size of a closed population within which a non-zoonotic person-to-person pathogen can persist indefinitely. In other words, it is the total size of the population (of susceptible and infected individuals, or others) necessary to sustain an outbreak once it has appeared.

## Superspreading

An event in which an infectious disease spreads much more than usual. Likewise, an individual who disproportionately infects a large number of individuals and likely drives the speed and severity of an outbreak is known as a superspreader.

## Vectorial Transmission

Vectorial transmission means that an infection can be transmitted from a vector (e.g., mosquitoes) to humans. Examples of vector-borne diseases include malaria and dengue. The World Health Organization has a [fact sheet](https://www.who.int/news-room/fact-sheets/detail/vector-borne-diseases) on vector-borne diseases with key information and a list of them according to their vector.

## Viral Shedding

**Viral shedding** is the process by which a virus is released from the infected organism into the environment, where it can potentially infect other individuals. This phenomenon is fundamental in the transmission of viral diseases, as it determines when and how an infected person can be contagious.

## Pathogenicity

**Pathogenicity** is the ability of an infectious agent, such as a virus, bacterium, fungus, or parasite, to cause disease in a host. This ability depends on several factors inherent to the infectious agent and its interaction with the host. Pathogenicity is evaluated qualitatively, meaning whether a microorganism is capable of causing disease or not.

Characteristics of Pathogenicity:
* **Ability to Cause Disease:** Not all microorganisms are pathogenic; pathogenicity indicates whether an organism can cause disease under normal conditions.
* **Mechanisms of Pathogenicity:** Includes various biological processes that allow the infectious agent to invade and harm the host, such as adhesion to host cells, tissue invasion, immune system evasion, and toxin production.

## Virulence

**Virulence** is a quantitative measure of the severity of the disease caused by an infectious agent. It represents the intensity of the pathogenicity of a microorganism, that is, its ability not only to infect but also to cause significant harm to the host. Often, virulence is evaluated in terms of mortality rate, symptom severity, and impact on host health.

Characteristics of Virulence:
* **Severity of Disease:** Quantifies the harm a pathogen can cause to the host, including symptom severity and mortality rate.
* **Virulence Factors:** Molecules and mechanisms that allow the pathogen to invade the host, evade its immune system, and cause harm. These include toxins, enzymes, adhesion proteins, and immune evasion mechanisms.

## Natural Resistance

**Natural resistance** to a pathogen refers to the inherent ability of an organism to avoid infection or combat an infectious agent without the need for prior exposure, vaccination, or treatment. This resistance can be the result of various biological and genetic characteristics of the host that prevent the entry, replication, or spread of the pathogen.

Characteristics of Natural Resistance:
* **Inherent:** It is an innate characteristic of the organism, present without the need for prior exposure to the pathogen.
* **Genetic:** Often, natural resistance is determined by genetic factors that can vary among individuals and populations.
* **Pathogen-Specific:** Natural resistance can be specific to certain pathogens while others may not be affected.

Example: In studies conducted in Sub-Saharan Africa, it has been observed that populations with a high percentage of Duffy-negative individuals have a very low incidence of *Plasmodium vivax* infections. In contrast, in regions of Asia and South America, where most people are Duffy-positive, *Plasmodium vivax* malaria is more common.

## Infestation

Is a term used for a host affected by ectoparasites, fleas for example. Also to refer to infestation by insects or reservoirs in houses or places (the house is infested with bed bugs, the city is infested with rats, the infestation rate is 10%).

## Patent Infection

Is the period during which the infectious agent has not yet produced any signs or symptoms, but is already detectable by some means in the host.

## Latent or Subclinical Infection

The infectious agent is present in the host, but there is no indication of its presence. This state is very difficult to differentiate from incubation in the host.

## Sick

The host presents pathological signs or symptoms.

## Carrier

Is a prolonged infective state, with persistent elimination of the infectious agent. It can be a sick carrier, convalescent carrier, or healthy carrier.

## Immune

Possesses active or passive protection, cell and/or humorally mediated against infection.

## Active Immunity

Immunity due to previous exposure to antigens of the agent or similar to it.

## Passive Immunity

Immunity due to the transfer of antibodies, maternal or of other origin.

## Host Range

Those species of organisms that are naturally susceptible to a certain infectious agent.

## Reservoir

Species or populations that are capable of maintaining a certain infectious agent in nature.

## Definitive Host

The one in which the sexual reproduction of the agent takes place, when it has an obligatory sexual phase in its life cycle. This occurs in many helminths and protozoa.

## Intermediate Host

When the life cycle involves two different host species, this term describes the host in which the asexual phase of reproduction takes place.

## Amplifying Host

A host species that develops periodic epidemics by a certain agent, and that generates an increase in the size of the agent population large enough to spread to other species not usually exposed to that agent.

## Dead-end Host

Those species or species whose individuals are infected but are not functionally infective, and therefore do not transmit the infection.

## Duration of Infectivity

Is directly related to the time during which the infected host excretes considerable amounts of the infectious agent.

## Relapse or Recrudescence

Implies the recurrence of clinical signs after a period of inapparent or subclinical illness.

## Vertical Transmission

Implies the direct transfer of an infectious agent from a parent to offspring, either transplacentally or transovarially.

## Horizontal Transmission

Refers to the direct transfer of the pathogen from someone other than the parents.


# REFERENCIAS

-   Alzate, A. (1996). Conceptos básicos de enfermedades infecciosas.
    Boletín SIEI, 2(2), 2-5

-   Cambridge English Dictionary. (n.d.). Shedding. En Cambridge English
    Dictionary. Recuperado de <https://dictionary.cambridge.org>

-   Epiverse-Trace. (n.d.). Glossary. Recuperado de
    <https://epiverse-trace.github.io/tutorials-late/reference.html#glossary>

-   Glosario epidemiológico. Gobierno de
    Mexico. <https://www.insp.mx/nuevo-coronavirus-2019/glosario-epidemiologico.html> 

-   [Hart, William S., Elizabeth Miller, Nick J. Andrews, Pauline
    Waight, Philip K. Maini, Sebastian Funk, and Robin N.
    Thompson. 2022. "Generation Time of the Alpha and Delta SARS-CoV-2
    Variants: An Epidemiological Analysis." The Lancet Infectious
    Diseases 22 (5): 603--10.](http://paperpile.com/b/uKZiEn/PspE)

-   Holmdahl, I., & Buckee, C. (2020). COVID-19 epidemic prediction and
    the impact of public health interventions: A review of COVID-19
    epidemic models. ScienceDirect. Recuperado de
    <https://www.sciencedirect.com>

-   Keeling, M. J., & Rohani, P. (2008). A primer on stochastic epidemic
    models: Formulation, numerical simulation, and analysis.
    ScienceDirect. Recuperado de <https://www.sciencedirect.com>

-   Kucharski, A. J., & Edmunds, W. J. (2018). Key data for outbreak
    evaluation: Building on the Ebola experience. Philosophical
    Transactions of the Royal Society B: Biological Sciences. Recuperado
    de <https://royalsocietypublishing.org>

-   Lloyd-Smith, J. O., Schreiber, S. J., Kopp, P. E., & Getz, W. M.
    (2005). Superspreading and the effect of individual variation on
    disease emergence. Nature. Recuperado de <https://www.nature.com>

-   Math Insight. (n.d.). An introduction to ordinary differential
    equations. Recuperado de <https://mathinsight.org>

-   Milwid, R. (2016, 28 septiembre). Toward Standardizing a Lexicon of
    Infectious Disease Modeling Terms.
    Frontiers. <https://www.frontiersin.org/articles/10.3389/fpubh.2016.00213/full> 

-   Nishiura, H., Linton, N. M., & Akhmetzhanov, A. R. (2020). Serial
    interval of novel coronavirus (COVID-19) infections. International
    Journal of Infectious Diseases. Recuperado de
    <https://www.ijidonline.com>

-   Organización Panamericana de la Salud. COVID-19, GLOSARIO SOBRE
    BROTES Y EPIDEMIAS. PAHO.
    <https://www.paho.org/es/documentos/covid-19-glosario-sobre-brotes-epidemias-recurso-para-periodistas-comunicadores> 

-   Organización Panamericana de la Salud. Módulo de Principios de
    Epidemiología para el Control de Enfermedades (MOPECE) Segunda
    Edición Revisada. Unidad 5. Investigación epidemiológica de campo:
    aplicación al estudio de brotes.
    <https://www3.paho.org/hq/index.php?option=com_content&view=article&id=9161:2013-mopece-training-modules-epidemiology&Itemid=0&lang=es#gsc.tab=0> 

-   Park, S. (n.d.). Epidist-paper. GitHub. Recuperado de
    <https://github.com>

-   Wellcome Open Research. (n.d.). Estimating the overdispersion in
    COVID-19. Recuperado de <https://wellcomeopenresearch.org>

-   World Health Organization. (n.d.). Vector-borne diseases. Recuperado
    de <https://www.who.int>

-   [Wu, Yu, Liangyu Kang, Zirui Guo, Jue Liu, Min Liu, and Wannian
    Liang. 2022. "Incubation Period of COVID-19 Caused by Unique
    SARS-CoV-2 Strains: A Systematic Review and Meta-Analysis." JAMA
    Network Open 5 (8): e2228008.](http://paperpile.com/b/uKZiEn/yGCE)
