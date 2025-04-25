README – Replication Package for “Artificial Intelligence health advice accuracy varies across languages and contexts”

This directory contains all code needed to reproduce our analyses. For full package, including data, visit the Zenodo repository

Files:
  • project.Rproj  
  • 1_translate_health_claims.ipynb  
  • 2_classify_health_claims_with_openai.ipynb  
  • 3_evaluate_health_claim_predictions.Rmd  
  • 4_classify_pubhealth_with_openai.ipynb  
  • 5_evaluate_pubhealth_predictions.Rmd  

Directories:
  • data/       – Raw input files  (missing in GitHub version)
  • int_data/   – Processed and intermediary data  (missing in GitHub version)
  • figures/    – Final figures used in main text  (missing in GitHub version)

Purpose of each file:
1_translate_health_claims.ipynb  
  • Demonstrates how we translate UK/EU Health Claims Register entries into 21 languages  
  • Shows the OpenAI prompts and workflows used for translation  

2_classify_health_claims_with_openai.ipynb  
  • Illustrates how we classify translated health claims (supported vs. refuted) with OpenAI models  

4_classify_pubhealth_with_openai.ipynb  
  • Illustrates how we classify PUBHEALTH dataset claims using the same prompt structure  

Notes on notebooks 1_, 2_ and 4_:  
  • Provided for illustration only; not intended to be re-run end-to-end.  
  • All prompts and model settings (including for Ollama open-source models and Gemini) are identical across implementations—only operational code differs.  
  • Initial, intermediary, and final data files have been saved in int_data/ so that analyses can proceed without re-running notebooks 1_, 2_, or 4_.  

3_evaluate_health_claim_predictions.Rmd  
  • Loads processed health-claim classification outputs from int_data/  
  • Computes accuracy metrics and generates Figure 1  

5_evaluate_pubhealth_predictions.Rmd  
  • Loads processed PUBHEALTH classification outputs from int_data/  
  • Computes inaccuracy heatmaps and generates Figure 2  

Each code file contains additional inline documentation describing inputs, outputs, and step-by-step methods. Please open project.Rproj in RStudio to set the working directory and manage package dependencies.
