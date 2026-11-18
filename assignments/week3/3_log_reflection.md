# log and reflection

## part 1: work log

| step | work completed |
|---|---|
| think | reviewed the cleaned dataset and wrote an initial referee's note using the recorded prices and calculated statistics. |
| ask | used ai to interpret the statistics and provide possible explanations for the observed price changes. |
| check | compared the ai's claims with the dataset and calculations, separating supported observations from unsupported explanations. |
| explain | considered why the mean and median can give different impressions of a typical price. |
| reflect | reviewed the initial interpretation and identified where conclusions needed to be more cautious. |

## part 2: ai interpretation audit

| ai claim / interpretation | colour | how i checked it | verdict |
|---|---|---|---|
| "staple a mean price increased by 12.98% from 104.0 pkr to 117.5 pkr." | green | recalculated the percentage change: ((117.5 - 104.0) / 104.0) × 100 = 12.98%. these are the first and last recorded daily average prices. | accepted (observation) |
| "stores kept median prices steady by promoting generic brands." | red | the dataset can be used to compare median prices, but it contains no information about store promotions or generic-brand strategies. | rejected (unsupported explanation) |
| "the rise in staple a proves living costs worsened across both cities." | red | checked the other items and considered the dataset's limited coverage. a change in one item does not establish a wider change in living costs across both cities. | rejected (overreach) |

## part 3: confused classmate transcript excerpt

**classmate (ai):** if staple a went up by around 13%, why might someone still describe prices as steady using the median?

**me:** because the mean and median measure prices differently. the mean uses every observation, while the median represents the middle observation.

**classmate (ai):** but why does that matter? shouldn't one unusually high price affect both?

**me:** it affects the mean more directly because the mean includes the actual value of every observation. the median depends on the middle position, so one extreme value usually has less influence on it.

**classmate (ai):** so the median completely ignores unusually high prices?

**me:** not exactly. the values are still part of the dataset, but a single extreme value usually does not move the middle observation very much. it depends on the data.

**classmate (ai):** then should we always use the median instead of the mean?

**me:** no. both are useful. comparing them gives us a better understanding of the data than relying on just one measure.

## part 4: reflection

my initial analysis was more careful than some of the possible explanations produced during the ai interpretation stage. however, comparing the claims made me realise how easily statistical observations can turn into assumptions about the real world.

for example, the dataset can show that staple a's recorded average price increased, but it cannot prove that living costs worsened across both cities. similarly, it does not contain information about store promotions, generic brands or the reasons behind price changes.

the comparison between the mean and median was also useful. an unusual value can pull the mean upwards more strongly than the median, which shows why both measures should be considered when interpreting prices.

overall, this assignment helped me understand that calculating statistics is only one part of data analysis. it is equally important to question explanations, verify claims against the available evidence and avoid conclusions that the data cannot support.

## part 5: execution note

the pandas installation was unsuccessful in my python 3.14 environment. therefore, i included the analysis code in `2_work.ipynb`, but could not execute the notebook or verify its outputs in that environment.