# Cell-to-Cell Communication: Basophil to B cell via IL4

## Biological question
Can a basophil send an IL4 signal to a B cell, and what does the database evidence say about how it works?

## Sender cell and context
Basophil, in allergic (type 2) inflammation.

## Candidate ligand and sender evidence
- Ligand: IL4 (Interleukin-4), a secreted cytokine
- HPA immune cell data: IL4 RNA is highest in basophils in the HPA and Monaco datasets
- UniProt: lists basophils as a source of IL4
- Caveat: T cells also make IL4
- Signaling type: paracrine


![sender evidence](figures/01_sender_cell_evidence.png)



## Receptor and receiver cell
- Receptor: IL4R (with IL2RG)
- Receiver cell: naive B cell
- Evidence: HPA shows IL4R is highest in naive B cells in three datasets. UniProt says IL4R couples to JAK/STAT6 and regulates IgE production.
- Caveat: IL4R is also found in other cells, such as neutrophils. Choosing B cells is partly my own reasoning.

## OmniPath findings
- IL4 is annotated as a secreted ligand and cytokine (consensus score 21)
- Directed IL4 -> IL4R interaction with many references


![omnipath](figures/02_omnipath_evidence.png)



## STRING network
- Proteins: IL4, IL4R, IL2RG, JAK1, JAK3, STAT6 (6 nodes, 15 edges, PPI enrichment p = 8.97e-14)
- Top terms: interleukin-4-mediated signaling pathway (GO:0035771, FDR 2.6e-16), JAK-STAT signaling (KEGG hsa04630, FDR 4.96e-11)
- Note: I chose these proteins myself, so this supports the pathway but does not discover it. A STRING edge is not proof of direct binding.


![string](figures/03_string_network.png)



## IntAct validation
- IL4 and IL4R, Homo sapiens, in vitro
- X-ray diffraction, PMID 10219247, direct interaction
- ITC, PMID 18243101, direct interaction (Kd about 1 nM)
- Conclusion: direct physical binding is supported, but only in vitro.


![intact](figures/04_intact_evidence.png)



## Final model and interpretation


![model](figures/05_final_model.png)


(paste your 150-250 word interpretation here)

## Strong vs inferred
- Strong: IL4 binds IL4R, JAK-STAT pathway
- Inferred: basophils signal to B cells in the body, IgE class switching as the response

## References and links
- HPA: https://www.proteinatlas.org/
- OmniPath: https://omnipathdb.org/
- STRING: https://string-db.org/
- IntAct: https://www.ebi.ac.uk/intact/
- UniProt: https://www.uniprot.org/
