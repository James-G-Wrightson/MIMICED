# Naming aid: k-means with k = 8

KMeans(n_clusters=8, random_state=42, n_init=10) on the 80-component PCA matrix (chiefcomp_pca80.npy); labels in chiefcomp_clustered_k8.parquet. Written by 2_chiefcomp.ipynb (alternative-k sensitivity section).

## Cluster 0

**Size:** 62,280 (14.7% of complaints)

**Top 20 bigrams/trigrams (count):** shortness breath (3,129); urinary retention (1,486); dyspnea exertion (1,385); influenza like (1,282); like illness (1,282); influenza like illness (1,282); asthma exacerbation (1,167); cough dyspnea (877); unable ambulate (866); slurred speech (740); abnormal labs (635); respiratory distress (539); dyspnea transfer (533); unsteady gait (532); mental status (530); altered mental (527); altered mental status (527); dyspnea cough (520); cough fever (516); difficulty swallowing (507)

**Top 10 cleaned complaints (count):**

1. `dyspnea` (7,426)
2. `weakness` (3,527)
3. `dizziness` (3,020)
4. `shortness breath` (2,238)
5. `palpitations` (1,929)
6. `cough` (1,925)
7. `dysuria` (1,390)
8. `diarrhea` (1,139)
9. `urinary retention` (1,105)
10. `asthma exacerbation` (829)

**Stored 12-cluster labels feeding it** (complaints, share of this cluster):

- 4 Shortness breath: 46,551 (74.7%)
- 1 Influenza like illness: 8,286 (13.3%)
- 3 Chest pain + dyspnea: 3,088 (5.0%)
- 2 Vehicle collision + Altered mental status: 2,692 (4.3%)
- 0 Lower back pain: 748 (1.2%)
- 7 Wound evaluation: 663 (1.1%)

## Cluster 1

**Size:** 52,531 (12.4% of complaints)

**Top 20 bigrams/trigrams (count):** abdomen pain (28,987); abdominal pain (11,830); quadrant abdominal (6,449); quadrant abdominal pain (6,447); flank pain (6,101); lower quadrant (4,588); lower quadrant abdominal (4,459); upper quadrant (2,749); pain transfer (2,120); upper quadrant abdominal (1,989); lower abdominal (1,738); lower abdominal pain (1,733); abdomen pain transfer (1,634); epigastric pain (1,462); abdominal distention (1,252); back pain (1,215); sided abdominal (1,168); sided abdominal pain (1,164); rectal pain (1,101); pain diarrhea (970)

**Top 10 cleaned complaints (count):**

1. `abdomen pain` (15,996)
2. `flank pain` (3,505)
3. `lower quadrant abdominal pain` (2,967)
4. `abdominal pain` (2,002)
5. `abdomen pain transfer` (1,560)
6. `upper quadrant abdominal pain` (1,228)
7. `epigastric pain` (1,140)
8. `lower abdominal pain` (878)
9. `sided abdominal pain` (799)
10. `abdomen pain diarrhea` (796)

**Stored 12-cluster labels feeding it** (complaints, share of this cluster):

- 5 Abdomen pain: 51,062 (97.2%)
- 0 Lower back pain: 1,056 (2.0%)

## Cluster 2

**Size:** 17,576 (4.1% of complaints)

**Top 20 bigrams/trigrams (count):** fall transfer (1,565); injury fall (1,110); pain fall (1,109); head injury (992); hip pain (752); head injury fall (557); fracture fall (515); fall head (506); back pain (456); hip pain fall (442); fall hip (390); fall head injury (369); rib pain (294); fall hip pain (289); fracture fall transfer (281); back pain fall (276); hip fracture (253); laceration fall (251); head lac (251); fall laceration (250)

**Top 10 cleaned complaints (count):**

1. `fall` (8,090)
2. `fall transfer` (997)
3. `head injury fall` (511)
4. `hip pain fall` (419)
5. `fall head injury` (338)
6. `fall hip pain` (269)
7. `back pain fall` (255)
8. `laceration fall` (226)
9. `fall laceration` (223)
10. `fall weakness` (185)

**Stored 12-cluster labels feeding it** (complaints, share of this cluster):

- 11 Fall transfer: 16,536 (94.1%)
- 0 Lower back pain: 591 (3.4%)
- 6 Leg + knee pain: 284 (1.6%)

## Cluster 3

**Size:** 27,945 (6.6% of complaints)

**Top 20 bigrams/trigrams (count):** chest pain (26,441); pain dyspnea (2,589); chest pain dyspnea (2,572); pain transfer (850); pain cardiac (843); cardiac features (843); chest pain cardiac (843); pain cardiac features (843); chest pain transfer (828); back pain (761); rib pain (635); pain cough (582); pain palpitations (515); chest pain cough (510); chest pain palpitations (484); pain chest (475); dyspnea chest (471); dyspnea chest pain (471); pain chest pain (466); arm pain (367)

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

- 3 Chest pain + dyspnea: 26,074 (93.3%)
- 0 Lower back pain: 1,550 (5.5%)

## Cluster 4

**Size:** 72,197 (17.0% of complaints)

**Top 20 bigrams/trigrams (count):** wound evaluation (6,044); sore throat (3,893); neck pain (3,715); shoulder pain (3,343); arm pain (2,707); eye pain (2,043); ear pain (1,758); head injury (1,662); vehicle collision (1,426); finger laceration (1,423); hand injury (1,370); hand pain (1,132); wrist pain (1,076); facial swelling (1,075); finger injury (1,046); dental pain (1,037); back pain (934); like illness (929); influenza like (928); influenza like illness (928)

**Top 10 cleaned complaints (count):**

1. `headache` (5,722)
2. `wound evaluation` (5,105)
3. `fever` (3,581)
4. `sore throat` (2,186)
5. `rash` (2,171)
6. `shoulder pain` (1,760)
7. `neck pain` (1,473)
8. `arm pain` (1,381)
9. `finger laceration` (1,341)
10. `eye pain` (1,333)

**Stored 12-cluster labels feeding it** (complaints, share of this cluster):

- 2 Vehicle collision + Altered mental status: 22,943 (31.8%)
- 0 Lower back pain: 17,601 (24.4%)
- 7 Wound evaluation: 15,633 (21.7%)
- 1 Influenza like illness: 14,912 (20.7%)

## Cluster 5

**Size:** 45,608 (10.7% of complaints)

**Top 20 bigrams/trigrams (count):** back pain (12,878); leg pain (6,096); lower back (5,388); lower back pain (5,379); knee pain (4,976); foot pain (4,079); leg swelling (3,075); hip pain (2,180); ankle pain (2,180); pain leg (1,619); ankle injury (1,420); lower extremity (1,227); pain fall (1,156); toe pain (1,115); calf pain (1,009); bilateral leg (1,004); wound evaluation (827); pain leg pain (827); pain transfer (732); foot injury (687)

**Top 10 cleaned complaints (count):**

1. `back pain` (4,983)
2. `lower back pain` (3,365)
3. `knee pain` (3,084)
4. `leg pain` (2,841)
5. `foot pain` (2,585)
6. `hip pain` (1,524)
7. `ankle pain` (1,460)
8. `ankle injury` (1,171)
9. `leg swelling` (1,161)
10. `toe pain` (780)

**Stored 12-cluster labels feeding it** (complaints, share of this cluster):

- 6 Leg + knee pain: 30,341 (66.5%)
- 0 Lower back pain: 14,665 (32.2%)

## Cluster 6

**Size:** 122,961 (29.0% of complaints)

**Top 20 bigrams/trigrams (count):** alcohol intoxication (10,638); suicidal ideation (8,395); mental status (5,180); altered mental (5,057); altered mental status (5,048); vehicle collision (4,497); abnormal labs (3,818); influenza like (2,644); like illness (2,644); influenza like illness (2,644); allergic reaction (2,257); vaginal bleeding (1,754); unable ambulate (1,629); intoxication unable (1,469); alcohol intoxication unable (1,469); intoxication unable ambulate (1,465); substance use (1,097); psych evaluation (1,065); abnormal ct (910); pedestrian struck (909)

**Top 10 cleaned complaints (count):**

1. `suicidal ideation` (5,132)
2. `alcohol intoxication` (4,707)
3. `vehicle collision` (3,637)
4. `altered mental status` (3,169)
5. `syncope` (2,905)
6. `seizure` (2,814)
7. `influenza like illness` (2,452)
8. `abnormal labs` (2,382)
9. `brbpr` (2,296)
10. `allergic reaction` (1,903)

**Stored 12-cluster labels feeding it** (complaints, share of this cluster):

- 7 Wound evaluation: 61,054 (49.7%)
- 2 Vehicle collision + Altered mental status: 22,434 (18.2%)
- 8 Alcohol intoxication: 12,121 (9.9%)
- 10 Suicidal ideation: 11,476 (9.3%)
- 3 Chest pain + dyspnea: 6,547 (5.3%)
- 1 Influenza like illness: 6,063 (4.9%)
- 4 Shortness breath: 1,805 (1.5%)
- 11 Fall transfer: 1,391 (1.1%)

## Cluster 7

**Size:** 23,609 (5.6% of complaints)

**Top 20 bigrams/trigrams (count):** nausea vomiting (14,486); abdomen pain (6,763); pain nausea (5,881); pain nausea vomiting (4,463); abdomen pain nausea (4,428); pain vomiting (1,125); abdomen pain vomiting (872); headache nausea (858); dizziness nausea (784); vomiting abdomen (744); vomiting abdomen pain (739); abdominal pain (687); chest pain (668); nausea vomiting abdomen (651); vomiting nausea (476); fever nausea (474); alcohol intoxication (443); epigastric pain (440); headache nausea vomiting (425); dizziness nausea vomiting (358)

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

- 9 Nausea vomiting: 23,068 (97.7%)
- 8 Alcohol intoxication: 433 (1.8%)
