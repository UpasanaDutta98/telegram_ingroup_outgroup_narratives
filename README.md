# Framing the Fringe: Ingroup and Outgroup Narratives in Fringe Telegram Channels

Dataset release for the paper:

> **Framing the Fringe: Dynamics of Ingroup and Outgroup Narratives in Fringe Telegram Channels**  
> Upasana Dutta, Yasmine Houri  
> *18th ACM Web Science Conference (WebSci '26), May 26–29, 2026, Braunschweig, Germany*  
> DOI: [10.1145/3795766.3799784](https://doi.org/10.1145/3795766.3799784)

## Dataset

We release message IDs and LLM-generated annotations for ~294,000 Telegram messages collected between March 2024 and February 2025, across 292 channels in five categories/themes.

Raw message text is **not included** in compliance with Telegram's Terms of Service. Researchers can hydrate the dataset using the provided `channel_id` and message `id` via the [Telethon](https://github.com/LonamiWebs/Telethon) library:

> Note: hydration completeness may degrade over time if messages or channels are deleted.

## Annotations

Each message is annotated along three dimensions using a GPT-5-nano zero-shot classification framework:

id	channel_id	channel_name	date	

| Field | Description |
|---|---|
| id | message id |
| channel_id | channel id |
| channel_name | channel name |
| date | date of posting |
| `Standardized_Core_Stance_Label` | Ingroup Heroism, Ingroup Victimhood, Outgroup Moral Condemnation, Outgroup Threat, Outgroup Hate, or None |
| `Standardized_Outgroup_Target_Type` | Political/Cultural Group, Social/Ethnic Group, Institutions & Elites, Unspecified Enemy, or None |
| `Standardized_Ingroup_Focus_Type_Label` | Political/Ideological Activism, Social/Ethnic Group, Institutions & Elites, National Citizens, Unspecified, or None |
| `Standardized_Emotional_Intensity_Label` | 1–5 scale |

Annotations were validated against human labels (see paper for more details).

## Files

```
data/
├── covid_dataset.csv
├── qanon_dataset.csv
├── white_dataset.csv
├── maga_dataset.csv
└── proudboys_dataset.csv
```

## Citation

```bibtex
@inproceedings{dutta2026framing,
  title     = {Framing the Fringe: Dynamics of Ingroup and Outgroup Narratives in Fringe Telegram Channels},
  author    = {Dutta, Upasana and Houri, Yasmine},
  booktitle = {18th ACM Web Science Conference (WebSci '26)},
  year      = {2026},
  doi       = {10.1145/3795766.3799784}
}
```

## Disclaimer

This dataset contains annotations of Telegram messages from hateful and conspiratorial communities. The dataset is released strictly for research purposes. The authors do not endorse any of the views expressed in the original messages.
