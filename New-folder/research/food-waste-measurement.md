# Food-Waste Measurement: A Practical Research and Baseline Guide

| Field | Details |
|---|---|
| Ticket | ANN-R-002 |
| Documentation area | Research Context |
| Status | Research draft; ANNAPURNA's actual sites, activities and data requirements need confirmation |
| Intended audience | Development team and people involved in data collection |
| Owner listed in tracker | Vasantha |
| Tracker references | REF-ANN-01, REF-ANN-02 and REF-ANN-32 (the source files or links were not provided) |
| File | `docs/research/food-waste-measurement.md` |

## 1. Why a consistent approach matters

If you want to know whether food waste is changing, you have to record it the same way every time. Each record should show what was thrown away, where it came from, how much there was and when it was measured. Leave those details out and comparisons between sites or time periods can easily mislead.

This guide is a practical starting point for the ANNAPURNA team. It explains the main terms, helps you decide what a measurement should include, compares common methods and lists what to capture in each record. It also covers a simple site procedure and some checks that keep the data dependable.

A lot is still unknown. The tracker doesn't say which sites or sectors are involved, which food categories to include or what equipment is available. Everything below is therefore a proposed approach, not a description of a system ANNAPURNA already uses. The internal reference IDs in the tracker weren't supplied as documents or links either.

## 2. Be clear about what you're measuring

### 2.1 Food waste

Under the UNEP Food Waste Index, food waste means food, along with its associated inedible parts, that leaves the human food supply chain at the retail, food-service or household stage. It can include raw ingredients, partly processed food, prepared meals and drinks. Bones, rinds and fruit stones are examples of associated inedible parts.

What counts as edible varies with local food habits. So the team should write down the classification it's using instead of assuming every site treats the same part of a food item the same way.

It's also worth noting where the discarded material ends up: composted, sent for digestion or land application, flushed to the sewer, burned under controlled conditions, or thrown out with general waste and sent to landfill. Knowing the destination tells you more than weight alone.

### 2.2 Food loss and food waste are different things

People often use the two terms together, but SDG indicator 12.3.1 splits them by stage of the supply chain:

- **Food loss (12.3.1(a)):** FAO's Food Loss Index covers losses from after harvest up to, but not including, retail.
- **Food waste (12.3.1(b)):** UNEP's Food Waste Index covers retail and consumer stages, including food service and households.

The stage affects both the method you pick and how you report. Start by working out where the food is lost or discarded. If you cover more than one stage, keep the records separate so the same material isn't counted twice.

### 2.3 Keep food apart from everything else

For the records to be useful, treat these as separate material types:

- **Food:** Items or ingredients meant for people to eat, even if they later spoiled or became unsafe.
- **Associated inedible parts:** Bones, peels, pits and similar parts that aren't normally eaten in the setting being studied.
- **Packaging and other non-food material:** Plastic, paper, containers and the like. Take these out of food-waste totals or record them separately.

Where you can, weigh edible food and inedible parts separately. If you can't separate them, say so in the record.

## 3. Set the measurement boundary before you collect anything

A measurement boundary spells out exactly what the figures include. Agree on the points below first, so everyone works to the same scope:

| What to decide | What to record | Example |
|---|---|---|
| Site or group | The exact place or unit being measured | One named canteen, shop, household sample or facility |
| Location | The geographical area covered | A named site, town or district |
| Sector and supply-chain stage | Where the food is handled or discarded | Food service, retail or household |
| Food categories | Which kinds of food are included | All food, or a defined list of food groups |
| Material type | Whether food and inedible parts are included | Record food and inedible parts separately where possible |
| Destination | Where the discarded material goes | Compost, landfill, sewer, digestion or another recorded route |
| Measurement period | Start and end dates, and the days covered | `YYYY-MM-DD` to `YYYY-MM-DD`, with operating days noted |
| Unit | The main reporting unit | Kilograms (kg) |
| Measurement method | How the quantity is worked out | Weighing, sorting, counting, records or another method |
| Comparison basis | What activity the waste is compared with | Meals served, food purchased, production volume, households or operating days |

If ANNAPURNA ends up covering several sectors, report each one on its own before thinking about a combined total. A household, a restaurant and a shop all work differently, so their waste figures may need different comparison measures.

## 4. Ways to measure food waste

No single method suits every site. The best choice depends on the type of waste, the equipment and staff you have, how much time data collection can take and how accurate you need to be. This table compares the common options.

| Method | How it works | When it may be useful | Things to watch for |
|---|---|---|---|
| Direct weighing | Waste goes on a suitable scale and the weight is recorded. | Sites where waste can be collected and separated before disposal. | Subtract the container weight, keep packaging out of the total and use the same procedure each time. |
| Waste-composition analysis | A mixed waste sample is sorted into categories and each category is weighed. | Sites where food is mixed in with other waste. | Sampling and sorting have to be consistent, and staff need to follow safe handling procedures. |
| Counting or scanning | Discarded items are counted and converted to weight using known item weights. | Retail or other settings where individual products can be identified. | Use reliable, locally appropriate item weights and explain how you converted. |
| Volume estimate | The space the waste takes up is measured and converted to an estimated weight. | Situations where there's no scale. | Food density changes with moisture, shape and compaction, so the conversion can be uncertain. |
| Existing records | Purchase, stock, production, collection or disposal records are reviewed. | Organisations that already keep useful operational records. | These may miss some waste streams, or may have been created for another purpose. |
| Diaries or logs | Participants record what they throw away and how much over a set period. | Understanding day-to-day patterns in homes or workplaces. | People estimate quantities differently. Clear instructions and checks help. |
| Surveys or interviews | People are asked what they throw away and why. | Learning about habits, causes and possible improvements. | Self-reported answers help explain the problem, but they don't replace direct measurement when you need accurate quantities. |

**A practical starting point:** if it's safe and feasible to collect the material, weigh it directly. That gives you a measured quantity. Logs, diaries or short interviews can then explain why the waste happens. If direct weighing isn't possible, pick the next-best method for that setting and be upfront about where its estimates may be less accurate.

## 5. What to put in each baseline record

The fields below could form the basis of a spreadsheet or data-collection form. They cover what you need to identify a measurement, understand how it was taken and check it later. The final list can change once the sites and method are known.

| Field | Priority | What it's for |
|---|---|---|
| `record_id` | Essential | A unique ID for each record so it can be found and checked later. |
| `measurement_date` | Essential | The date the food was measured or the waste was generated (`YYYY-MM-DD`). |
| `measurement_start` / `measurement_end` | Useful | The time period or shift the record covers. |
| `site_id` / `site_name` | Essential | Identifies the site or sampled unit. Use a consistent ID. |
| `sector` | Essential | The setting, such as household, food service or retail. |
| `lifecycle_stage` | Essential | Where in the food supply chain the waste occurred. |
| `food_category` | Essential | The agreed food group. Add an explanation when using `Other`. |
| `food_item` | Useful | The specific item, when that level of detail is available. |
| `material_type` | Essential | Food, associated inedible part, or mixed/unknown. |
| `edible_classification` | Useful | Edible, inedible, mixed or not assessed, based on a documented rule. |
| `gross_weight_kg` | Required when weighing with a container | Weight of the waste together with its container. |
| `container_tare_kg` | Required when weighing with a container | Weight of the empty container. |
| `net_food_waste_kg` | Essential for weight-based records | Actual weight of the waste after subtracting the container and excluding non-food material. |
| `measurement_method` | Essential | Whether the figure came from weighing, sorting, a count conversion, an estimate or existing records. |
| `scale_id` / `calibration_check` | Useful for weighing | Identifies the scale and records that it was checked before use. |
| `destination` | Essential where known | Where the material went. Use `Unknown` rather than guessing. |
| `cause` | Useful | A likely reason, such as spoilage, overproduction, preparation waste, plate leftovers, damage or expired stock. |
| `denominator_value` | Essential for rate calculations | The comparison figure, such as meals served or kilograms of food purchased. |
| `denominator_unit` | Essential for rate calculations | The unit for the comparison figure. |
| `collector_id` | Useful | The person or team collecting the data. Protect personal information. |
| `sample_id` | Useful for sample-based work | Links the record to a particular sample, batch or sampling exercise. |
| `evidence_reference` | Useful | Points to a weighing sheet, source record or approved evidence file. |
| `data_quality_flag` | Useful | Marks the record as validated, estimated, incomplete, unusual or awaiting review. |
| `notes` | Useful | Unusual conditions, exclusions, corrections or other context. |

### Example record (for illustration only)

| record_id | date | site | sector | category | material | net kg | method | destination | denominator |
|---|---|---|---|---|---|---:|---|---|---:|
| DEMO-0001 | 2026-11-01 | SITE-DEMO | Food service | Cooked rice | Food | 2.40 | Direct weighing | Compost | 120 meals |

This row is made up. It only shows the format. It isn't an ANNAPURNA measurement and mustn't be used as project evidence.

## 6. A repeatable way to measure waste at a site

1. **Confirm the scope first.** Agree on the site, food categories, waste streams, dates, material types and destinations before anyone starts measuring.
2. **Check the scale.** Make sure it suits the expected weights and reads zero before use. Follow the manufacturer's guidance for routine checks, and record the scale ID.
3. **Keep materials separate.** Use labelled containers where you can. Food, inedible parts, packaging and other waste shouldn't end up in the same measurement.
4. **Note when you measured.** Record the date, start and end times, shift or meal period, and anything unusual about operations that day.
5. **Weigh the same way every time.** If you use a container, record its weight and subtract it from the combined weight. If the material changes before weighing (say, water gets added), make a note.
6. **Describe the material.** Record the food category, whether it's food or an inedible part, where it went and, if known, why it was thrown away.
7. **Capture a comparison figure.** A canteen might record the number of meals served in the same period. Other sites may need food purchased, production volume or operating days instead.
8. **Review the entries.** Look for missing fields, duplicate IDs, wrong units, negative net weights and values that look off. Mark estimates clearly so nobody confuses them with direct measurements.
9. **Keep the supporting evidence.** Store weighing sheets or approved digital records under a clear evidence ID. Don't collect personal information unless you really need it.
10. **Write down anything that may have affected the result.** That could be a missed collection, a scale problem, a menu change or a switch in method.

## 7. Making baseline results comparable

A baseline is the reference point the team will check later results against. For the comparison to mean anything, keep the scope, food categories, method, units, measurement period and comparison figure as consistent as you can.

For instance, a follow-up might show less waste simply because it covered fewer days or used a different method. That's why any change in the process has to be documented and taken into account when you compare results.

Pick a baseline period that looks as much like normal operations as possible. Depending on the site, you may need weekdays and weekends, different shifts or seasonal changes. A few days of data shouldn't automatically be treated as representative of a whole year.

### Basic calculations

Let:

- `gross_weight_kg` be the weight of the waste together with its container;
- `container_tare_kg` be the weight of the empty container; and
- `net_food_waste_kg` be the weight of the waste itself.

**Net food-waste weight**

`net_food_waste_kg = gross_weight_kg - container_tare_kg`

**Total waste recorded during the period**

`total_food_waste_kg = SUM(net_food_waste_kg)`

**Waste per meal** (only when meals served is a suitable comparison figure)

`food_waste_kg_per_meal = total_food_waste_kg / meals_served`

**Food-waste percentage of food input** (only when both figures cover the same scope and use the same unit)

`food_waste_rate_percent = (food_waste_kg / food_input_kg) * 100`

Always say what the denominator stands for. A percentage based on food purchased isn't the same as one based on food prepared or served.

### Worked example (not project data)

Say a site records 12 kg of food waste while serving 600 meals:

`12 kg / 600 meals = 0.020 kg per meal = 20 g per meal`

This only illustrates the calculation. It's not a result from an ANNAPURNA site.

## 8. Sampling and estimates

Measuring every household, shop or site may not be practical. If the team uses a sample, it should choose locations that reasonably represent the wider group it wants to understand, not just the ones that are easiest to get to.

The report should explain:

- Which group or population the sample is meant to represent.
- How the sample was chosen, and what counts as one sampling unit (a site, household, shift or collection route, for example).
- How many sites or participants were included.
- When and how the measurements were made.
- Any missing records, non-responses or waste streams that were left out.
- How the sample results were used to estimate a larger total, if that was done.
- What uncertainty or limitations apply to the estimate.

Don't take a small convenience sample, multiply it up to the whole population and present the result as a verified total. Scaling up needs a suitable sampling method, and the final report must explain the uncertainty and limitations.

## 9. Checks that keep the data reliable

Before the figures go into a report, make sure that you:

- Use the same names and categories for sectors, lifecycle stages, food types, methods and destinations.
- Use one standard unit, preferably kilograms, and one date format.
- Label estimated or self-reported figures so they aren't mistaken for directly measured weights.
- Check the container weight and confirm the net weight isn't negative.
- Keep packaging and other non-food material out of food-waste totals, or explain how it was separated.
- Confirm the same waste hasn't been counted at more than one point as it moves through collection and disposal.
- Keep the original entry and note any corrections rather than quietly replacing the value.
- Record unknown or missing information as such. Don't enter zero when you simply don't know the value.
- Review unusual values and, where possible, compare totals with other available records.
- Note any changes to the method, equipment, categories or instructions between the baseline and later measurements.

## 10. Questions the ANNAPURNA team needs to answer

Before the form is finalised, the team should settle these:

1. Which sector and supply-chain stage will the project cover?
2. Which sites, locations or groups will be included?
3. Is the team measuring food waste, food loss, surplus food recovery or more than one of these? If more than one, how will the records be kept separate?
4. Which food categories and waste streams should be included?
5. Can edible food and associated inedible parts be weighed separately?
6. Which destinations need to be recorded?
7. Is direct weighing possible? What equipment and staff are available?
8. What comparison figure makes sense for the site: meals served, food purchased, production volume, households or operating days?
9. What measurement period will give a fair picture of normal operations?
10. Who will collect the data, check it and store the records?
11. What consent, privacy, safety and access requirements apply to the sites or people involved?
12. What original documents or links were meant by REF-ANN-01, REF-ANN-02 and REF-ANN-32?

## 11. References

These references provide the public research behind this guide. They are **not** the internal REF-ANN-* files named in the tracker, which still need to be supplied or marked as unavailable.

1. United Nations Environment Programme (UNEP). **Food Waste Index Report 2024.** https://wedocs.unep.org/handle/20.500.11822/45230
2. United Nations Statistics Division. **Metadata for SDG Indicator 12.3.1(b), Food Waste Index.** https://unstats.un.org/sdgs/metadata/files/Metadata-12-03-01B.pdf
3. UNEP. **SDG Indicator 12.3.1: Food Loss Index and Food Waste Index.** https://sdgs.unep.org/article/sdg-indicator-1231
4. Food and Agriculture Organization of the United Nations (FAO). **Food loss measurement.** https://www.fao.org/platform-food-loss-waste/food-loss/food-loss-measurement/
5. Food Loss and Waste Protocol. **Food Loss and Waste Accounting and Reporting Standard.** https://flwprotocol.org/flw-standard/
6. World Resources Institute (WRI). **Food Loss and Waste Accounting and Reporting Standard.** https://www.wri.org/research/food-loss-and-waste-accounting-and-reporting-standard
7. Food Loss and Waste Protocol. **Sample Reporting Template.** https://flwprotocol.org/flw-standard/tools-resources/sample-reporting-template/

## 12. Review checklist

- [ ] The measurement boundary and site scope have been agreed.
- [ ] Food loss and food waste are used consistently.
- [ ] The chosen method suits the site and the type of waste.
- [ ] The people collecting the data have reviewed the fields and categories.
- [ ] The baseline period and comparison figure have been decided.
- [ ] Direct measurements and estimates are clearly labelled.
- [ ] Any sampling method and its limits are explained.
- [ ] Test records have been checked for missing, duplicate or unrealistic values.
- [ ] The missing internal references have been supplied, or their absence has been recorded.
- [ ] The development and data-collection teams have reviewed the document, and the tracker has been updated.
