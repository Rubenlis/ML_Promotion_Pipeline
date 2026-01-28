# ML_Promotion_Pipeline


A pipeline where every new trained model:

Trains + logs to MLflow

Registers a new model version in the MLflow Model Registry

Deploys staging API that serves models:/<name>/Staging

Runs quality gates (accuracy threshold, plus smoke tests placeholder)

If you decide it’s good, you promote that version to Production (manual workflow)

Production API serves models:/<name>/Production (registry is the source of truth)
