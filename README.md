# query-now
sample query at sql
SET @startdate = '2021-09-01';
SET @enddate = '2021-09-16';

SELECT
date,`hour`,vendor,site_cellid,siteid,
total_traffic,
rrc_connected,
s1_signaling,
LastTTI,
avail,
cell_dl_peak,
user_dl_avg,
rrc,
erab,
rank2_ratio,
dl_prb,
se_dl,
cqi,
qpsk_ratio,
avg_ue_distance_avg,
erab_drop,
rbler_dl,
packet_delay,
packet_loss,
intra_ho,
inter_ho,
csfb_exec,
`L.E-RAB.FailEst.NoRadioRes.RrcUserLic`

FROM
4g_combine_hr_kpi
WHERE
date >= @startdate
