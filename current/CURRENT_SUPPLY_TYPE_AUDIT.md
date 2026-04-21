# Current Supply Type Audit

wb_supply_id: WB-GI-232323720
detected_type: FBS
source: local_payload_prefix_analysis
risk: critical
decision: DO_NOT_USE_WRONG_TYPE
can_be_used_for_fbo_handover: no
can_get_fbw_box_labels: no
can_get_supply_barcode: no
next_action: Пересоздать поставку с deliveryType=fbo. python -m app.cli wb recreate-current-supply --mode dry-run
fox2box_handover_allowed: false
label_workflow_blocked: true
audited_at: 2026-04-21T04:09:06Z
