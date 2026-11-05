# Naming aid: k-means with k = 14

KMeans(n_clusters=14, random_state=42, n_init=10) on the 80-component PCA matrix (chiefcomp_pca80.npy); labels in chiefcomp_clustered_k14.parquet. Written by 2_chiefcomp.ipynb (alternative-k sensitivity section).

## Cluster 0

**Size:** 14,321 (3.4% of complaints)

**Top 20 bigrams/trigrams (count):** like illness (5,152); influenza like (5,151); influenza like illness (5,151); sore throat (678); cough fever (548); fever influenza (504); fever influenza like (502); cough influenza (502); cough influenza like (500); fever cough (384); fever transfer (344); fever headache (338); wound evaluation (255); chest pain (249); fever weakness (237); body aches (223); fever sore (222); fever sore throat (222); pain influenza (217); pain influenza like (216)

**Top 10 cleaned complaints (count):**

1. `fever` (3,581)
2. `influenza like illness` (2,452)
3. `cough fever` (359)
4. `cough influenza like illness` (332)
5. `fever influenza like illness` (276)
6. `fever cough` (266)
7. `fever headache` (265)
8. `fever transfer` (265)
9. `fevers` (213)
10. `fever weakness` (209)

**Stored 12-cluster labels feeding it** (complaints, share of this cluster):

- 1 Influenza like illness: 14,022 (97.9%)

## Cluster 1

**Size:** 30,842 (7.3% of complaints)

**Top 20 bigrams/trigrams (count):** leg pain (5,336); knee pain (4,958); foot pain (4,019); leg swelling (2,918); ankle pain (2,159); hip pain (2,006); ankle injury (1,575); toe pain (1,125); calf pain (973); bilateral leg (935); pain leg (901); pain fall (881); wound evaluation (796); foot injury (684); knee injury (611); foot swelling (539); pain wound (504); pain wound evaluation (503); bilateral leg swelling (503); leg weakness (494)

**Top 10 cleaned complaints (count):**

1. `knee pain` (3,084)
2. `leg pain` (2,841)
3. `foot pain` (2,585)
4. `hip pain` (1,524)
5. `ankle pain` (1,460)
6. `ankle injury` (1,171)
7. `leg swelling` (1,161)
8. `toe pain` (780)
9. `calf pain` (683)
10. `foot injury` (526)

**Stored 12-cluster labels feeding it** (complaints, share of this cluster):

- 6 Leg + knee pain: 30,241 (98.1%)

## Cluster 2

**Size:** 32,025 (7.5% of complaints)

**Top 20 bigrams/trigrams (count):** alcohol intoxication (11,213); suicidal ideation (8,532); mental status (4,272); altered mental (4,162); altered mental status (4,154); unable ambulate (1,623); intoxication unable (1,471); alcohol intoxication unable (1,471); intoxication unable ambulate (1,467); substance use (1,053); depression suicidal (738); pain alcohol (493); pain alcohol intoxication (491); intoxication fall (488); alcohol intoxication fall (488); homicidal ideation (482); substance misuse (458); misuse intoxication (452); substance misuse intoxication (452); depression suicidal ideation (443)

**Top 10 cleaned complaints (count):**

1. `suicidal ideation` (5,132)
2. `alcohol intoxication` (4,707)
3. `altered mental status` (3,169)
4. `alcohol intoxication unable ambulate` (1,423)
5. `anxiety` (1,332)
6. `hyperglycemia` (1,109)
7. `depression` (846)
8. `overdose` (631)
9. `substance use` (595)
10. `substance misuse intoxication` (447)

**Stored 12-cluster labels feeding it** (complaints, share of this cluster):

- 8 Alcohol intoxication: 12,689 (39.6%)
- 10 Suicidal ideation: 11,616 (36.3%)
- 2 Vehicle collision + Altered mental status: 6,002 (18.7%)
- 7 Wound evaluation: 1,345 (4.2%)

## Cluster 3

**Size:** 48,446 (11.4% of complaints)

**Top 20 bigrams/trigrams (count):** abnormal labs (3,253); psych evaluation (832); abnormal ct (826); subarachnoid hemorrhage (808); unknown cc (725); gi bleed (626); gtube evaluation (555); mental status (534); altered mental (523); altered mental status (522); ich transfer (492); abnormal mri (450); suture removal (440); seizure transfer (439); med refill (433); cva transfer (418); sdh transfer (412); hemorrhage transfer (390); subarachnoid hemorrhage transfer (389); picc line (376)

**Top 10 cleaned complaints (count):**

1. `abnormal labs` (2,382)
2. `brbpr` (2,296)
3. `cp` (1,430)
4. `` (1,427)
5. `hypertension` (1,142)
6. `transfer` (894)
7. `unknown cc` (725)
8. `psych evaluation` (711)
9. `abscess` (608)
10. `lightheaded` (566)

**Stored 12-cluster labels feeding it** (complaints, share of this cluster):

- 7 Wound evaluation: 44,954 (92.8%)
- 2 Vehicle collision + Altered mental status: 2,846 (5.9%)

## Cluster 4

**Size:** 20,934 (4.9% of complaints)

**Top 20 bigrams/trigrams (count):** vaginal bleeding (2,108); urinary retention (1,699); rectal pain (1,129); flank pain (784); pelvic pain (746); testicular pain (661); urinary frequency (507); abdominal pain (439); lower abdominal (367); lower abdominal pain (367); vaginal pain (350); pregnant vaginal (346); pregnant vaginal bleeding (322); pain urinary (286); abnormal labs (276); back pain (274); pain dysuria (229); dysuria flank (204); dysuria flank pain (204); rectal bleeding (201)

**Top 10 cleaned complaints (count):**

1. `dysuria` (1,390)
2. `hematuria` (1,241)
3. `diarrhea` (1,139)
4. `vaginal bleeding` (1,118)
5. `urinary retention` (1,105)
6. `rectal pain` (788)
7. `constipation` (616)
8. `anemia` (612)
9. `testicular pain` (567)
10. `pelvic pain` (518)

**Stored 12-cluster labels feeding it** (complaints, share of this cluster):

- 7 Wound evaluation: 7,471 (35.7%)
- 4 Shortness breath: 6,177 (29.5%)
- 5 Abdomen pain: 3,682 (17.6%)
- 1 Influenza like illness: 1,920 (9.2%)
- 0 Lower back pain: 1,376 (6.6%)

## Cluster 5

**Size:** 41,794 (9.8% of complaints)

**Top 20 bigrams/trigrams (count):** abdomen pain (28,228); abdominal pain (5,759); flank pain (5,061); upper quadrant (2,708); quadrant abdominal (2,034); quadrant abdominal pain (2,033); pain transfer (2,014); upper quadrant abdominal (1,969); abdomen pain transfer (1,633); epigastric pain (1,371); abdominal distention (1,183); sided abdominal (1,147); sided abdominal pain (1,143); pain diarrhea (894); abdomen pain diarrhea (873); chest pain (764); pain fever (655); back pain (593); pain abnormal (583); abdomen pain fever (559)

**Top 10 cleaned complaints (count):**

1. `abdomen pain` (15,996)
2. `flank pain` (3,505)
3. `abdominal pain` (2,002)
4. `abdomen pain transfer` (1,560)
5. `upper quadrant abdominal pain` (1,228)
6. `epigastric pain` (1,140)
7. `sided abdominal pain` (799)
8. `abdomen pain diarrhea` (796)
9. `abdomen pain fever` (454)
10. `abdominal distention` (382)

**Stored 12-cluster labels feeding it** (complaints, share of this cluster):

- 5 Abdomen pain: 41,682 (99.7%)

## Cluster 6

**Size:** 22,834 (5.4% of complaints)

**Top 20 bigrams/trigrams (count):** back pain (14,368); abdominal pain (5,656); lower back (5,619); lower back pain (5,608); lower quadrant (4,994); quadrant abdominal (4,367); quadrant abdominal pain (4,366); lower quadrant abdominal (4,365); lower abdominal (1,288); lower abdominal pain (1,283); pain lower (775); lower extremity (730); leg pain (688); pain leg (687); back pain leg (650); extremity pain (592); lower extremity pain (588); pain fall (541); pain transfer (525); quadrant pain (506)

**Top 10 cleaned complaints (count):**

1. `back pain` (4,983)
2. `lower back pain` (3,365)
3. `lower quadrant abdominal pain` (2,967)
4. `lower abdominal pain` (878)
5. `lower extremity pain` (543)
6. `lower quadrant pain` (446)
7. `body pain` (355)
8. `back pain transfer` (278)
9. `breast pain` (266)
10. `back pain fall` (255)

**Stored 12-cluster labels feeding it** (complaints, share of this cluster):

- 0 Lower back pain: 16,535 (72.4%)
- 5 Abdomen pain: 5,765 (25.2%)
- 6 Leg + knee pain: 435 (1.9%)

## Cluster 7

**Size:** 59,976 (14.1% of complaints)

**Top 20 bigrams/trigrams (count):** shortness breath (3,098); dyspnea exertion (1,353); asthma exacerbation (1,141); unable ambulate (867); cough dyspnea (831); slurred speech (798); mental status (725); altered mental (722); altered mental status (722); abnormal labs (720); respiratory distress (600); unsteady gait (540); dyspnea transfer (535); dyspnea cough (504); failure thrive (501); chest pain (453); leg swelling (451); difficulty swallowing (403); dyspnea hypoxia (402); weakness transfer (382)

**Top 10 cleaned complaints (count):**

1. `dyspnea` (7,426)
2. `weakness` (3,527)
3. `dizziness` (3,020)
4. `syncope` (2,905)
5. `shortness breath` (2,238)
6. `palpitations` (1,929)
7. `cough` (1,925)
8. `epistaxis` (956)
9. `presyncope` (889)
10. `asthma exacerbation` (829)

**Stored 12-cluster labels feeding it** (complaints, share of this cluster):

- 4 Shortness breath: 41,447 (69.1%)
- 3 Chest pain + dyspnea: 9,118 (15.2%)
- 1 Influenza like illness: 4,390 (7.3%)
- 2 Vehicle collision + Altered mental status: 3,073 (5.1%)
- 7 Wound evaluation: 1,564 (2.6%)

## Cluster 8

**Size:** 31,285 (7.4% of complaints)

**Top 20 bigrams/trigrams (count):** neck pain (3,705); sore throat (3,318); shoulder pain (2,425); eye pain (1,967); ear pain (1,729); dental pain (1,002); vehicle collision (889); facial swelling (841); facial numbness (771); jaw pain (504); visual changes (500); dizziness headache (480); collision neck (459); vehicle collision neck (459); collision neck pain (446); facial pain (444); foreign body (413); headache neck (408); headache neck pain (395); body sensation (389)

**Top 10 cleaned complaints (count):**

1. `headache` (5,722)
2. `sore throat` (2,186)
3. `shoulder pain` (1,760)
4. `neck pain` (1,473)
5. `eye pain` (1,333)
6. `ear pain` (1,095)
7. `dental pain` (722)
8. `facial swelling` (529)
9. `facial numbness` (390)
10. `dizziness headache` (390)

**Stored 12-cluster labels feeding it** (complaints, share of this cluster):

- 2 Vehicle collision + Altered mental status: 19,935 (63.7%)
- 0 Lower back pain: 6,534 (20.9%)
- 1 Influenza like illness: 4,093 (13.1%)

## Cluster 9

**Size:** 37,074 (8.7% of complaints)

**Top 20 bigrams/trigrams (count):** wound evaluation (5,636); vehicle collision (5,028); allergic reaction (2,222); head injury (1,781); pedestrian struck (921); visual changes (740); dog bite (459); cardiac arrest (440); facial droop (417); head bleed (348); collision transfer (345); vehicle collision transfer (342); bicycle accident (316); abdo pain (282); eye redness (273); pain vehicle (271); pain vehicle collision (271); eye evaluation (256); vision changes (249); cat bite (248)

**Top 10 cleaned complaints (count):**

1. `wound evaluation` (5,105)
2. `vehicle collision` (3,637)
3. `seizure` (2,814)
4. `rash` (2,171)
5. `allergic reaction` (1,903)
6. `head injury` (1,211)
7. `assault` (1,126)
8. `confusion` (922)
9. `pedestrian struck` (829)
10. `laceration` (694)

**Stored 12-cluster labels feeding it** (complaints, share of this cluster):

- 2 Vehicle collision + Altered mental status: 15,902 (42.9%)
- 7 Wound evaluation: 13,553 (36.6%)
- 1 Influenza like illness: 4,877 (13.2%)
- 11 Fall transfer: 1,371 (3.7%)
- 0 Lower back pain: 659 (1.8%)
- 3 Chest pain + dyspnea: 530 (1.4%)

## Cluster 10

**Size:** 15,790 (3.7% of complaints)

**Top 20 bigrams/trigrams (count):** fall transfer (1,525); head injury (933); hip pain (745); pain fall (674); injury fall (638); head injury fall (544); fall head (488); fracture fall (483); hip pain fall (440); fall hip (388); fall head injury (358); rib pain (299); fall hip pain (287); fracture fall transfer (273); hip fracture (250); head lac (242); fall laceration (235); laceration fall (231); fall sdh (207); fall weakness (202)

**Top 10 cleaned complaints (count):**

1. `fall` (8,090)
2. `fall transfer` (997)
3. `head injury fall` (511)
4. `hip pain fall` (419)
5. `fall head injury` (338)
6. `fall hip pain` (269)
7. `laceration fall` (226)
8. `fall laceration` (223)
9. `fall weakness` (185)
10. `head lac fall` (171)

**Stored 12-cluster labels feeding it** (complaints, share of this cluster):

- 11 Fall transfer: 15,605 (98.8%)

## Cluster 11

**Size:** 23,282 (5.5% of complaints)

**Top 20 bigrams/trigrams (count):** nausea vomiting (14,475); abdomen pain (6,761); pain nausea (5,862); pain nausea vomiting (4,463); abdomen pain nausea (4,428); pain vomiting (1,160); abdomen pain vomiting (869); headache nausea (844); dizziness nausea (782); vomiting abdomen (743); vomiting abdomen pain (738); abdominal pain (696); chest pain (665); nausea vomiting abdomen (651); vomiting nausea (476); fever nausea (474); epigastric pain (439); headache nausea vomiting (425); dizziness nausea vomiting (358); vomiting weakness (351)

**Top 10 cleaned complaints (count):**

1. `nausea vomiting` (4,567)
2. `abdomen pain nausea vomiting` (3,196)
3. `vomiting` (871)
4. `abdomen pain vomiting` (801)
5. `abdomen pain nausea` (778)
6. `nausea vomiting abdomen pain` (580)
7. `nausea` (577)
8. `vomiting nausea` (411)
9. `headache nausea vomiting` (306)
10. `headache nausea` (294)

**Stored 12-cluster labels feeding it** (complaints, share of this cluster):

- 9 Nausea vomiting: 23,011 (98.8%)

## Cluster 12

**Size:** 18,926 (4.5% of complaints)

**Top 20 bigrams/trigrams (count):** arm pain (2,661); finger laceration (1,424); hand injury (1,394); wrist pain (1,260); hand pain (1,129); finger injury (1,062); elbow pain (842); arm numbness (831); pain fall (711); shoulder pain (700); arm swelling (610); wrist injury (590); hand laceration (560); hand swelling (540); shoulder injury (519); thumb laceration (508); finger pain (488); upper extremity (470); pain arm (425); thumb injury (397)

**Top 10 cleaned complaints (count):**

1. `arm pain` (1,381)
2. `finger laceration` (1,341)
3. `hand injury` (956)
4. `finger injury` (820)
5. `wrist pain` (755)
6. `hand pain` (656)
7. `thumb laceration` (483)
8. `elbow pain` (462)
9. `hand laceration` (456)
10. `finger pain` (334)

**Stored 12-cluster labels feeding it** (complaints, share of this cluster):

- 0 Lower back pain: 8,940 (47.2%)
- 7 Wound evaluation: 8,530 (45.1%)
- 11 Fall transfer: 634 (3.3%)
- 4 Shortness breath: 380 (2.0%)
- 2 Vehicle collision + Altered mental status: 217 (1.1%)

## Cluster 13

**Size:** 27,178 (6.4% of complaints)

**Top 20 bigrams/trigrams (count):** chest pain (25,887); pain dyspnea (2,588); chest pain dyspnea (2,573); pain transfer (846); pain cardiac (843); cardiac features (843); chest pain cardiac (843); pain cardiac features (843); chest pain transfer (824); rib pain (615); back pain (514); pain cough (495); pain palpitations (494); chest pain palpitations (481); dyspnea chest (474); dyspnea chest pain (474); chest pain cough (473); pain chest (446); pain chest pain (437); arm pain (354)

**Top 10 cleaned complaints (count):**

1. `chest pain` (14,189)
2. `chest pain dyspnea` (2,004)
3. `chest pain cardiac features` (843)
4. `chest pain transfer` (750)
5. `rib pain` (459)
6. `chest pain palpitations` (426)
7. `dyspnea chest pain` (392)
8. `chest pain cough` (323)
9. `chest pain dizziness` (316)
10. `chest pain arm pain` (261)

**Stored 12-cluster labels feeding it** (complaints, share of this cluster):

- 3 Chest pain + dyspnea: 25,789 (94.9%)
- 0 Lower back pain: 1,344 (4.9%)
