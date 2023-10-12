---
title: Payroll Taxes
date: 2023-08-28
description: This data story outlines the process for estimating the amount of payroll taxes nonprofits pay annually.
featured: true
featuredOrder: 1
type: methods
categories:
  - SOI extracts
  - payroll tax
author:
  - id: hmartin
  - id: jlecy
citation: 
  container-title: National Center for Charitable Statistics
  volume: 1
  issue: 1
  doi: 10.5555/12345678
links:
  - header: Replication Files
    links:  
    - text: Data + Code
      href: https://tinyurl.com/ylydvtj9
      icon: download
    - text: Code
      href: https://raw.githubusercontent.com/UrbanInstitute/nccs-recipes/main/vignettes/payroll.R
      icon: link
  - header: In Context 
    links:
    - text: Nonprofit Infrastructure Coalition 
      href: https://independentsector.org/wp-content/uploads/2023/04/nic-agenda-2023.pdf
      icon: download
---

The nonprofit sector is persistently striving to measure its scale of
activities to better understand its impact as well as convey the scale
of the work to key stakeholders to highlight societal benefits. Clear
ways of measuring activities can help engage policymakers and donors to
ensure support for the work is sustained.

How does one measure the size of the nonprofit sector? Researchers and
advocates commonly use counts of nonprofits, revenues, assets, and
program expenses. The mobilization of human resources, both paid and
volunteer, is perhaps a more salient measure of the depth of engagement
within communities but is has historically been a harder statistic to
generate due to limited reporting requirements (nonprofits report
estimates of employees on the 990 forms but they are not required to
differentiate part-time and full-time employees and the information has
not been systematically digitized until recently). Partnerships with the
Quarterly Census of Employment and Wages have helped more precisely
measure the size of the nonprofit workforce but estimates are currently
only updated every five years.

A less common but perhaps more accurate approach to measuring employment
levels is through payroll tax disclosures. Although most nonprofits are
exempt from federal income taxes they are still required to pay federal
payroll taxes. Taxes are levied for both part and full-time employees,
meaning the aggregate level of payroll taxes can be used to estimate the
number of full-time equivalent workers employed by the sector.

This data story estimates the amount of payroll taxes the nonprofit
sector contributes annually, in 2023 dollars.

To replicate our methodology, please see the tutorial at the end.

## Estimating Payroll Tax Contributions

To estimate the payroll taxes that the nonprofit sector contributes
annually, we use 2019 IRS 990 data, since it is the most recent full
year of available data. IRS Form 990 data extracts, available at
<https://www.irs.gov/statistics/soi-tax-stats-annual-extract-of-tax-exempt-organization-financial-data>.

We use 3 years of data extracts since there can be a 2-year lag in
returns being filed, so we first compile all of the 2019 990 returns
from across the 2019, 2020, and 2021 SOI extracts.

### Form 990 Data

The Internal Revenue Service (IRS) requires tax-exempt nonprofits to
file annual returns.

- Private foundations must file Form 990-PF.
- Most nonprofits must file Form 990, 990-EZ, or 990-N.
  - Those with gross receipts \>= \$200K or total assets \>= \$500K must
    file Form 990.
  - Those with gross receipts \<\$200K and total assets \<\$500K can
    file Form 990-EZ.
  - Those with gross receipts \<=\$50K can file Form 990-N.
- Some nonprofits, such as churches, do not have to file annual returns.
  See
  <https://www.irs.gov/charities-non-profits/annual-exempt-organization-return-who-must-file>.

### Data Limitations

What does Form 990 series tell us about the amount of payroll taxes that
nonprofits pay?

***Larger Nonprofits:*** The Form 990 collects data on the amount of
payroll taxes that larger nonprofits (i.e., those with gross receipts
\>= \$200K or total assets \>= \$500K) contribute (**\$55B in 2019**).

***Private foundations:*** The Form 990-PF does not collect data on the
amount of payroll taxes that private foundations contribute However, it
does collect data on the amount that private foundations spend on
salaries and benefits (\$3B). The Form 990 collects this data for larger
nonprofits, as well. Therefore, we can divide the amount of payroll
taxes that larger nonprofits contribute by the amount that larger
nonprofits spend on payroll taxes to calculate a payroll tax/salaries
and benefits ratio (5.75%). We can then apply that ratio to the salaries
and benefits data from the Form 990-PF to estimate the amount of payroll
taxes that private foundations contribute.

However, the IRS’s Form 990-PF data extract only includes the columns
with data on “compensation of officers, directors, trustees, etc.” and
“pension plans, employee benefits;” it excludes the column with data on
“other employee salaries and wages.” Therefore, we will underestimate
the amount of payroll taxes that private foundations contribute.
Additionally, the IRS does not provide a data extract for the 2019 Form
990-PF file. This creates a further underestimation of the amount of
payroll taxes that private foundations contribute (**estimated \$153M in
2019**).

***Smaller Nonprofits:*** The Form 990-EZ does not collect data on the
amount of payroll taxes that smaller nonprofits (i.e., those with gross
receipts \<\$200K and total assets \<\$500K) contribute It does collect
data on the amount that smaller nonprofits spend on salaries and
benefits, but the IRS’s Form 990-EZ data extracts exclude these data.
Therefore, we are unable to estimate the amount of payroll taxes that
smaller nonprofits contribute.

***Invisible Nonprofits:*** The Form 990-N does not collect data on the
amount of payroll taxes that the smallest nonprofits (i.e., those with
gross receipts \<=\$50K) contribute, nor does it collect data on the
amount that these nonprofits spend on salaries and benefits. Therefore,
we are unable to estimate the amount of payroll taxes that the smallest
nonprofits contribute.

We are also unable to estimate the amount of payroll taxes that
nonprofits that are not required to file annual returns contribute.

***Total:*** Adding the amount of payroll taxes that larger nonprofits
contributed in 2019 to the estimated amount of payroll taxes that
private foundations contributed in 2019 and adjusting 18.85% for
inflation (per <https://salaryinflation.com/>), **we estimate that the
nonprofit sector contributes \$66B annually in payroll taxes.** Although
this is a conservative estimate of payroll taxes, it demonstrates the
huge size and economic contributions of the nonprofit sector.

## Data Vignette

A tutorial that explains the process with links to replications files is
available here:

<a class="btn -tertiary " href="https://urbaninstitute.github.io/nccs-recipes/vignettes/payroll.html">
DATA VIGNETTE </a>

<br> <br>
<hr>

<br> <br>