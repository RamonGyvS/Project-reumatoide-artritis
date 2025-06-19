# Project-reumatoide-artritis
Project transcriptomics over reumatoide artritis, jaar 2 periode 4.

# 1. Inleiding
Reumatoïde artritis (RA) is een chronische ontstekingsziekte. Het valt onder de auto-immuunziektes waarbij het lichaam zichzelf aanvalt. Ontstekingen van RA ontstaat meestal in de gewrichten, het kan ook andere organen ontsteken. Klachten zijn pijn, en stijfheid van de gewrichten. Hierbij zit de patiënt veel stil en heeft moeite met bewegen, bij oudere patiënten kan dit weer leiden tot meer klachten. RA komt op alle leeftijden voor. Het komt meer voor bij vrouwen dan bij mannen, dit verschil is ongeveer 2 tot 1. Er is nog niet geconstateerd of RA een erfelijke ziekte is. Wel zijn er bepaalde genen die vaker voorkomen bij patiënten zoals HLA-DRB1, maar niet elk persoon met dit gen heeft de ziekte. Omgevingsfactoren zoals roken hebben we invloed op het ontwikkelen va RA. 
Hoewel de exacte etiologie van RA nog niet volledig is opgehelderd, wijst onderzoek op een complexe interactie tussen genetische aanleg (zoals *HLA-DRB1*-allelen), omgevingsfactoren (bijvoorbeeld roken) en auto-immuunreacties tegen gecitrullineerde peptiden (ACPA/anti-CCP) (Radu & Bungau, 2021). Een vroege diagnose en interventie zijn cruciaal om progressieve gewrichtsbeschadiging te remmen, maar de heterogeniteit van RA bemoeilijkt de identificatie van betrouwbare biomerkers (Majithia & Geraci, 2007). 

# 2. Materiaal en methode
Voor dit project zijn een aantal R-pakketten gebruikt voor de verwerking van data en statistische analyses. Voor het laten zien van de top 50 genen in een cluster heatmap is pheatmap gebruikt. Om de KEGG route hsa04064 te visualiseren is het pakket pathview gebruikt. Het lezen en manipuleren van data is gedaan met readr en dplyr. De reads alignen en tellen op gen-niveau is met Rsubread uitgevoerd. Het sorteren en indexeren van BAM-bestanden is met Rsamtools gedaan. DESeq2 heeft het differentieel expressie onderzoek gedaan. KEGGREST was voor de weg naar de pathway informatie. EnhancedVolcano is gebruikt voor het maken van volcano-plots. ClusterProfiler is gebruikt bij het KEGG verrijkings onderzoek. Daarnaast zijn goseq en geneLenDataBase gebruikt om het GO verrijkings onderzoek opnieuw met gene length bias correctie uit te voeren. Ook is org.Hs.eg.db gebruikt om tussen gen symbolen en ENTREZ ID’s te converteren. 

# 3. Resultaten
bla bla bla

# 4. Discussie
bla bla bla

# 5. Conclusie
bla bla bla

