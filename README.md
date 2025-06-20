# Project-reumatoide-artritis
Project transcriptomics over reumatoide artritis, jaar 2 periode 4.

# Inhoud
1. Inleiding
2. Materiaal en methode
3. Resutaten
4. Conclusie/discussie

# 1. Inleiding
Reumatoïde artritis (RA) is een chronische ontstekingsziekte. Het valt onder de auto-immuunziektes waarbij het lichaam zichzelf aanvalt. Ontstekingen van RA ontstaat meestal in de gewrichten, het kan ook andere organen ontsteken. Klachten zijn pijn, en stijfheid van de gewrichten. Er zijn bepaalde genen die vaker voorkomen bij patiënten zoals HLA-DRB1, maar niet elk persoon met dit gen heeft de ziekte.Hoewel de exacte etiologie van RA nog niet volledig is opgehelderd, wijst onderzoek op een complexe interactie tussen genetische aanleg, zoals: HLA-DRB1 allelen, omgevingsfactoren en auto-immuunreacties tegen gecitrullineerde peptiden (ACPA/anti-CCP) (Radu & Bungau, 2021). Een vroege diagnose en interventie zijn cruciaal om progressieve gewrichtsbeschadiging te remmen, maar de heterogeniteit van RA bemoeilijkt de identificatie van betrouwbare biomerkers (Majithia & Geraci, 2007). 
Voor het vroege behandelen van RA is er moet er inzicht komen in de genexpressie van patiënten. In dit onderzoek zijn er vier datasets geleverd van hoeveelheden genen van RA patienten, en vier controle monsters. Het monster is afkomstig uit het gewrichtsslijmvlies. Doormiddel van R studio is de data geanalyseerd doormiddel van verschillende pakages. Het doel van dit expiriment is: analyseren welke genen hoger of lager tot expressie komen in personen met Reumatoïde artritis, en welke metabole routes hierbij anders functioneren. 

# 2. Materiaal en methode
Voor dit project zijn een aantal R-pakketten gebruikt voor de verwerking van data en statistische analyses. Voor het laten zien van de top 50 genen in een cluster heatmap is pheatmap gebruikt. Om de KEGG route hsa04064 te visualiseren is het pakket pathview gebruikt. Het lezen en manipuleren van data is gedaan met readr en dplyr. De reads alignen en tellen op gen-niveau is met Rsubread uitgevoerd. Het sorteren en indexeren van BAM-bestanden is met Rsamtools gedaan. DESeq2 heeft het differentieel expressie onderzoek gedaan. KEGGREST was voor de weg naar de pathway informatie. EnhancedVolcano is gebruikt voor het maken van volcano-plots. ClusterProfiler is gebruikt bij het KEGG verrijkings onderzoek. Daarnaast zijn goseq en geneLenDataBase gebruikt om het GO verrijkings onderzoek opnieuw met gene length bias correctie uit te voeren. Ook is org.Hs.eg.db gebruikt om tussen gen symbolen en ENTREZ ID’s te converteren.
Voor het visualiseren van de genen zijn 3 verschillende plots gebruikt. Volcano plot: Op de x-as staat de log₂ fold change, en op de y-as de -log₁₀(p-waarde) ofwel, significantie. Groene punten zijn genen die zowel statistisch significant als sterk gereguleerd zijn. Rode punten zijn alleen gereguleerd, blauwe zijn niet significant. KEGG Enrichment Analysis: De x-as toont de verhouding van betrokken genen (GeneRatio). Kleur geeft de significantie aan (p.adj), en de grootte het aantal betrokken genen. Top 50 KEGG term plot: Deze grafiek toont de top KEGG terms/biologische pathways die geassocieerd zijn met de genen van patiënten met reuma. Y-as geeft significante pathways aan zoals de TNF signaling pathway, IL-17 signaling pathway, en "Rheumatoid arthritis. X-as geeft significantie aan (lengte = -log10(p-waarde)), waarbij langere balken een sterker verband aangeven. Hieronder een flowchart van het werkproces van dit onderzoek.
![Flowchart](Flowchart/Flowchart%20R%20Reuma.png)



# 3. Result
In de [volcano plot](./resultaten/R%20figuur%20volcano%20plot.png) zijn de genen met de hoogste log2 fold change te zien, dit zijn COL6A5, IGKV1-39, SRGN, BCL2A1 en PTGFR. Laag gereguleerde genen zijn MXRA7P1, IKBKGP1, MT-ND6 en ANKRD30BL.

Daarnaast toont de [KEGG E analyse](./resultaten/R%20KEGG%20E%20analyse.png)
 dat meerder pathways significante naar boven kwamen, dit waren MAPK signaling pathway, Epstein Barr virus, Lipid en atheroscerosis en NOD like receptor signaling pathway. 

# 4. Conclusie/discussie
Het doel van dit expiriment is: analyseren welke genen hoger of lager tot expressie komen in personen met Reumatoïde artritis, en welke metabole routes hierbij anders functioneren.

In het Volcano plot zijn SRGN, BCL2A1 en PTGFR gevonden als up-regulated genen, ook zijn deze vaak upregulated bij een onsteking in het lichaam. 

Als verbetering voor de volgende keer 




