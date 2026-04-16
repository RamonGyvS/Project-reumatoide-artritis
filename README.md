# PTGSD gen als vroege biomarker voor het behandelen van reumatoïde artritis

# Inhoud
1. Inleiding
2. Materiaal en methode
3. Resutaten
4. Conclusie/discussie

# 1. Inleiding
Reumatoïde artritis (RA) is een chronische ontstekingsziekte. Het valt onder de auto-immuunziektes waarbij het lichaam zichzelf aanvalt. Ontstekingen van RA ontstaat meestal in de gewrichten, het kan ook andere organen ontsteken. Klachten zijn pijn, en stijfheid van de gewrichten. Er zijn bepaalde genen die vaker voorkomen bij patiënten zoals HLA-DRB1, maar niet elk persoon met dit gen heeft de ziekte. Hoewel RA nog niet volledig bekend is als ziekte, wijzen onderzoeken op een  correlatie tussen genetische aanleg, omgevingsfactoren en auto-immuunreacties tegen gecitrullineerde peptiden (ACPA/anti-CCP) (Radu & Bungau, 2021). Een vroege diagnose is cruciaal om progressieve gewrichtsbeschadiging te remmen. Echter is dit complex, omdat RA een ziekte is met een diverse symtomen per patient is het vinden van betrouwbare biomarkers uitdagend (Majithia & Geraci, 2007). 
Voor het vroege behandelen van RA is er moet er inzicht komen in de genexpressie van patiënten. In dit onderzoek zijn er vier datasets geleverd van hoeveelheden genen van RA patienten, en daarbij vier controle monsters van gezonde mensen. Het monster is afkomstig uit het gewrichtsslijmvlies. Doormiddel van R studio is de data geanalyseerd doormiddel van verschillende pakages.
Het doel van dit expiriment is: analyseren welke genen hoger of lager tot expressie komen in personen met Reumatoïde artritis, en welke metabole routes hierbij anders functioneren. 

# 2. Materiaal en methode
Voor dit project zijn een aantal R-pakketten gebruikt voor de verwerking van data en statistische analyses. Om de KEGG route hsa04064 te visualiseren is het pakket pathview gebruikt. Het lezen en manipuleren van data is gedaan met readr en dplyr. De reads alignen en tellen op gen-niveau is met Rsubread uitgevoerd. Het sorteren en indexeren van BAM-bestanden is met Rsamtools gedaan. DESeq2 heeft het differentieel expressie onderzoek gedaan. KEGGREST was voor de weg naar de pathway informatie. EnhancedVolcano is gebruikt voor het maken van volcano-plots. ClusterProfiler is gebruikt bij het KEGG verrijkings onderzoek. Daarnaast zijn goseq en geneLenDataBase gebruikt om het GO verrijkings onderzoek opnieuw met gene length bias correctie uit te voeren. Ook is org.Hs.eg.db gebruikt om tussen gen symbolen en ENTREZ ID’s te converteren.
Voor het visualiseren van de genen zijn 3 verschillende plots gebruikt. Volcano plot: Op de x-as staat de log₂ fold change, en op de y-as de -log₁₀P. Groene punten zijn genen die zowel statistisch significant als sterk gereguleerd zijn. KEGG Enrichment Analysis: De x-as toont de verhouding van betrokken genen. Kleur geeft de significantie aan, en de grootte het aantal betrokken genen. Top 50 KEGG term plot: Deze grafiek toont de top KEGG terms/biologische pathways die geassocieerd zijn met de genen van patiënten met reuma. Y-as geeft significante pathways aan zoals de TNF signaling pathway, IL-17 signaling pathway, en "Rheumatoid arthritis. X-as geeft significantie aan (lengte = -log10P, waarbij langere balken een sterker verband aangeven. Hieronder een flowchart van het werkproces van dit onderzoek.

<img src="Flowchart/Flowchart%20R%20Reuma.png" width="750">

# 3. Resultaten
In de volcano plot:

<img src="./resultaten/R%20figuur%20volcano%20plot.png" width="750">

vallen de genen met de grootste log2 fold change op. De meest upregulated genen zijn *COL6A5, IGKV1-39, SRGN, BCL2A1* en *PTGFR*, terwijl *MXRA7P1, IKBKGP1, MT-ND6* en *ANKRD30BL* downregulated zijn. Het gaat hierbij om genen met een significant verschil in expressie tussen patiënten met reumatoïde artritis en controles.

Ook laten de KEGG analyse:

<img src="./resultaten/R%20KEGG%20E%20analyse.png" width="750">

en de top KEGG termen:

<img src="./resultaten/R%20top%20KEGG%20term.png" width="750">

zien dat meerdere biologische pathways significant verrijkt zijn. Belangrijke pathways zijn hierbij de MAPK signaling pathway, Epstein-Barr virus pathway, lipid and atherosclerosis pathway en de NOD-like receptor signaling pathway. Deze pathways zijn vooral betrokken bij immuunreacties en inflammatoire processen en passen bij het ziektebeeld van reumatoïde artritis.

Opvallend is dat *PTGDS* hogere expressie vertoont. Dit gen is betrokken bij ontstekingsprocessen en is daarom interessant voor verder onderzoek in deze studie.

# 4. Conclusie/discussie
In dit onderzoek is gekeken naar welke genen verschillend tot expressie komen bij patiënten met reumatoïde artritis en welke biologische pathways daarbij betrokken zijn. De resultaten laten zien dat meerdere genen, waaronder SRGN, BCL2A1 en PTGFR, verhoogd tot expressie komen bij RA-patiënten.
PTGDS valt hierbij op. Dit gen speelt een rol bij de productie van prostaglandine D2, een stof die betrokken is bij ontstekingsreacties. De verhoogde expressie van PTGDS kan erop wijzen dat het bijdraagt aan de chronische ontsteking die kenmerkend is voor reumatoïde artritis. Daarom zou PTGDS mogelijk gebruikt kunnen worden als biomarker om de ziekte in een vroeg stadium te herkennen (Ungethuem, 2010).

Het belangrijk om te benadrukken dat deze rol nog niet definitief is aangetoond en dat verdere validatie nodig is met betrekking tot PTGDS.
Een beperking van deze studie is dat er geen onderscheid is gemaakt tussen verschillende patiëntgroepen, zoals leeftijd, geslacht of genetische achtergrond. Daarnaast zou een grotere steekproef de betrouwbaarheid en statistische hoeveelheid van de resultaten kunnen verhogen.


