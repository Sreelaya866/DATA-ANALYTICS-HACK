# VoltRelay Energy: Network Performance & Service Diagnostic

An end-to-end data analytics and operational diagnostic investigation of **VoltRelay Energy’s** battery-swapping network across six Indian metropolitan markets (Bengaluru, Delhi NCR, Hyderabad, Pune, Mumbai, Jaipur), evaluating 3.9 million swap events between January 2024 and June 2025.

---

## 1. Executive Summary

Between January 2024 and June 2025, VoltRelay expanded its network through two major station rollout waves, brought on a new battery supplier (Kyron), renegotiated its primary B2B fleet contract, and piloted dynamic pricing[cite: 3, 4]. While monthly completed swaps surged from roughly 104,000 to over 300,000, the network experienced severe operational strain:
* **Seasonal Service Failure Spikes:** Failure rates repeatedly surged during summer months, peaking above 12% in May 2024 and over 9% in May 2025.
* **Thermal Charging Throttling:** When ambient temperatures exceed 40°C, battery recharge times jump from 70 minutes to over 125 minutes, draining charged inventory ahead of the evening peak.
* **Tariff & Capacity Cannibalization:** B2B partner fleet swaps yield the lowest unit contribution margin (₹41.50) but consume critical battery inventory during peak hours, crowding out retail riders who pay up to ₹65.20 per swap.
* **Hardware Degradation:** Sub-75% SOH battery packs see real-world range drop below 45 km, with supplier Kyron exhibiting high performance variance and lower median delivery.

---

## 2. Repository Structure

```text
├── README.md
├── notebooks/
│   └── voltrelay_analytics_pipeline.ipynb   # Complete Colab notebook (cleaning, EDA, charts)
├── docs/
│   ├── analysis_report.md                   # Full business report for leadership
│   └── presentation_script.md               # 3-minute video presentation script
└── figures/
    ├── network_performance_over_time.png    # Chart 1: Volume, margin, and failure trends
    ├── thermal_charging_bottlenecks.png     # Chart 2: Hourly failures & temperature vs charge time
    ├── battery_soh_vs_range.png             # Chart 3: Delivered range by SOH tier and supplier
    ├── margin_by_tariff_code.png            # Chart 4: Average contribution margin by tariff
    └── rider_churn_onboarding.png           # Chart 5: Early failure impact on rider drop-off
