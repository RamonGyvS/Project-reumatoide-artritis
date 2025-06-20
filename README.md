# Project-reumatoide-artritis
Project transcriptomics over reumatoide artritis, jaar 2 periode 4.

# 1. Inleiding
Reumatoïde artritis (RA) is een chronische ontstekingsziekte. Het valt onder de auto-immuunziektes waarbij het lichaam zichzelf aanvalt. Ontstekingen van RA ontstaat meestal in de gewrichten, het kan ook andere organen ontsteken. Klachten zijn pijn, en stijfheid van de gewrichten. Er zijn bepaalde genen die vaker voorkomen bij patiënten zoals HLA-DRB1, maar niet elk persoon met dit gen heeft de ziekte.Hoewel de exacte etiologie van RA nog niet volledig is opgehelderd, wijst onderzoek op een complexe interactie tussen genetische aanleg, zoals: HLA-DRB1 allelen, omgevingsfactoren en auto-immuunreacties tegen gecitrullineerde peptiden (ACPA/anti-CCP) (Radu & Bungau, 2021). Een vroege diagnose en interventie zijn cruciaal om progressieve gewrichtsbeschadiging te remmen, maar de heterogeniteit van RA bemoeilijkt de identificatie van betrouwbare biomerkers (Majithia & Geraci, 2007). Voor het vroege behandelen van RA is er moet er inzicht komen in de genexpressie van patiënten. In dit onderzoek zijn er vier datasets geleverd van hoeveelheden genen van RA patienten, en vier controle monsters. Het monster is afkomstig uit het gewrichtsslijmvlies. Doormiddel van R studio is de data geanalyseerd doormiddel van verschillende pakages. Het doel van dit expiriment is: analyseren welke genen hoger of lager tot expressie komen in personen met Reumatoïde artritis, en welke metabole routes hierbij anders functioneren. 

# 2. Materiaal en methode
Voor dit project zijn een aantal R-pakketten gebruikt voor de verwerking van data en statistische analyses. Voor het laten zien van de top 50 genen in een cluster heatmap is pheatmap gebruikt. Om de KEGG route hsa04064 te visualiseren is het pakket pathview gebruikt. Het lezen en manipuleren van data is gedaan met readr en dplyr. De reads alignen en tellen op gen-niveau is met Rsubread uitgevoerd. Het sorteren en indexeren van BAM-bestanden is met Rsamtools gedaan. DESeq2 heeft het differentieel expressie onderzoek gedaan. KEGGREST was voor de weg naar de pathway informatie. EnhancedVolcano is gebruikt voor het maken van volcano-plots. ClusterProfiler is gebruikt bij het KEGG verrijkings onderzoek. Daarnaast zijn goseq en geneLenDataBase gebruikt om het GO verrijkings onderzoek opnieuw met gene length bias correctie uit te voeren. Ook is org.Hs.eg.db gebruikt om tussen gen symbolen en ENTREZ ID’s te converteren. De

Volcano plot 
De volcano plot toont de expressieverandering van genen tussen reumapatiënten en controlepersonen. Op de x-as staat de log₂ fold change, en op de y-as de -log₁₀(p-waarde) ofwel, significantie. Groene punten zijn genen die zowel statistisch significant als sterk gereguleerd zijn. Rode punten zijn alleen gereguleerd, blauwe zijn niet significant. 
KEGG Enrichment Analysis
Dit dotplot laat zien welke biologische pathways (processen) verrijkt zijn onder de gedifferentieerde genen. De x-as toont de verhouding van betrokken genen (GeneRatio). Kleur geeft de significantie aan (p.adj), en de grootte het aantal betrokken genen. 
Top 50 genen (VST) heatmap
Deze heatmap toont de expressieniveaus van de 50 meest variabele genen (na variant-stabiliserende transformatie). Elke rij is een gen, elke kolom een sample (patiënt of controle). Rood = hoge expressie, blauw = lage expressie.
Clustering toont patronen en mogelijke groepen van genen die samen gereguleerd zijn. 
Top 50 KEGG term plot
Deze grafiek toont de top KEGG terms/biologische pathways die geassocieerd zijn met de genen van patiënten met reuma. Hoe kleiner de p-waarde, hoe sterker het verband met reuma. Y-as geeft significante pathways aan zoals de TNF signaling pathway, IL-17 signaling pathway, en "Rheumatoid arthritis. Deze zijn typisch betrokken bij ontstekingsprocessen en auto-immuniteit. X-as geeft significantie aan (lengte = -log10(p-waarde)), waarbij langere balken een sterker verband aangeven. Voor het VST-plot van de top 50 genen (variantie-stabiliserende transformatie) geld: Rood= hogere expressie (up), blauw = lagere expressie (down) in patiënten tegen de controles. Laat clustering zien om genen met vergelijkbare expressiepatronen worden gegroepeerd om biomarkers te indentificeren.


# 3. Resultaten
De genen zijn visueel gemaakt doormiddel van een volcanoplot, KEGG E analyse plot, top 50 genen VST plot en een top KEGG term plot.

In de grafiek is te zien dat er een aantal genen sterk up gereguleerde zijn, namelijk de genen: ANKRD30BL, ZNF598, CROCC, CLDN7AARSD1, BCL2A1, ACTBP4. 


# 4. Discussie
Het doel van dit expiriment is: analyseren welke genen hoger of lager tot expressie komen in personen met Reumatoïde artritis, en welke metabole routes hierbij anders functioneren.

# 5. Conclusie
Het doel van dit expiriment is: analyseren welke genen hoger of lager tot expressie komen in personen met Reumatoïde artritis, en welke metabole routes hierbij anders functioneren.

