; ================== FLUSH_START ==================
M400
T[next_extruder]                      ; Select next extruder

; --- Move to cutter ---
G1 E-5 F600
G1 X445 F9000
G1 X472.7 F400
M400 P2000
G1 E-1 F600
G1 Z{max(toolchange_z+2.6, 7.0)} F600

; --- Simple purge ---
G1 E9 F300
M106 S255
M400 P1200
M106 S0

; ===== Guaranteed X Recalibration =====
G1 E-1.5 F600                         ; Release pressure
G92 E0                                ; Reset extruder state
G28 X                                 ; Re-home X axis
M400
; =====================================

; --- Return to print ---
G1 Z{toolchange_z} F3000
M400
; ================== FLUSH_END ==================
