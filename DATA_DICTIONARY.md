# NeuroPsychAtlas field guide

Each association is identified by disease, sex, outcome and allele-specific variant. Available analyses are listed separately for each disease. Both denotes both sexes combined. Query P < 10⁻⁵ and discovery P < 5 × 10⁻⁹ serve distinct purposes.

| Field | Definition |
|---|---|
| `variant_key` | Allele-specific identifier, chromosome:position:REF:ALT. |
| `rsID` | dbSNP identifier where available. |
| `chromosome`, `position`, `genome_build` | GRCh38 variant location. |
| `REF`, `ALT` | Reference and alternate allele. |
| `effect_allele`, `other_allele` | REF and ALT, respectively, in the association model. |
| `beta_caf`, `se_caf` | RAF main-effect estimate and standard error per 0.01 increase in REF frequency; burden rates are per 100,000. The main effect is evaluated at SDI = 0. |
| `p_value`, `neg_log10_p` | Satterthwaite P value for the RAF main effect and its negative base-10 logarithm. |
| `df` | Degrees of freedom for the association test. |
| `ci_lower_caf`, `ci_upper_caf` | Bounds of the 95% confidence interval for βCAF. |
| `beta_interaction_caf`, `p_interaction` | RAF × SDI interaction coefficient and its P value. |
| `sdi_center` | SDI centring constant; zero for these analyses. |
| `beta_at_mean_sdi_caf`, `se_at_mean_sdi_caf` | RAF effect and its standard error at mean SDI. |
| `REF_AF_20country_pooled`, `ALT_AF_20country_pooled` | Frequencies calculated from pooled called allele counts across reference samples. |
| `MAF` | Minimum of pooled REF and ALT frequencies. |
| `n_rows`, `n_countries` | Country-year observations and countries used in the model. |
| `sex`, `measure`, `analysis_id` | Sex stratum, burden outcome and analysis identity; `analysis_id` is included in browser exports. |
| `is_lead`, `rank_lead` | Membership and rank in the discovery lead set; changing browser filters preserves these values. |
| `gene` | Mapped gene annotation where supplied. |
| `credible_status`, `causal_status` | Regional annotation labels where supplied; candidate prioritization does not establish causality. |
| `annotation_status`, `dbSNP_build` | Variant annotation information. |
| `status` | Availability of the association estimate. |

Empty cells represent unavailable values. A variant can occur in several analyses; the outcome and sex fields distinguish those records. Country views use REF frequencies between 0 and 1. Their displayed year-specific correlations describe the selected country data.


GBD tables retain national rates and uncertainty bounds. Regional results include Pearson r, P and BH-adjusted P. Enrichment tables retain P and BH-adjusted P.
