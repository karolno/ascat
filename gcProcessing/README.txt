############################
#GC correction file creation
############################

The script GCfileCreation.sh can help you create the input for ASCAT’s GC correction for platforms that are not yet provided.

./GCfileCreation.sh SNPpos SIZES CORES REF

SNPpos should contain the list of all probes with their genomic location (tab-separated).

	Chr	Position
rs3094315	1	752566
rs2073813	1	753541
rs2905040	1	770216
rs12124819	1	776546
rs2980314	1	781258

SIZES contains the length of all reference chromosomes. The annotation for hg19 can be found in the ASCAT repository.
With CORES you can define, how many cores to use for the computation. REF should provide the path to your local reference genome.

The created output file should start like this, with one row per provided probe:

	Chr	Position	25bp	50bp	100bp	200bp	500bp	1kb	2kb	5kb	10kb	20kb	50kb	100kb	200kb	500kb	1M	2M	5M	10M
rs3094315	1	752566	0.416667	0.44	0.36	0.36	0.406	0.435	0.428	0.4312	0.4447	0.42725	0.43452	0.44476	0.46216	0.502001	0.517331	0.520475	0.545639	0.52375
rs2073813	1	753541	0.625	0.48	0.51	0.49	0.5	0.484	0.497	0.4414	0.4601	0.4398	0.43728	0.4449	0.463805	0.50239	0.517472	0.520446	0.545618	0.52375
rs2905040	1	770216	0.208333	0.32	0.31	0.345	0.466	0.483	0.518	0.4914	0.4664	0.46845	0.45344	0.44179	0.47488	0.508137	0.522142	0.5197	0.545723	0.523597
rs12124819	1	776546	0.375	0.4	0.37	0.4	0.432	0.453	0.4375	0.4488	0.4642	0.4638	0.46552	0.44523	0.48165	0.51042	0.523123	0.519407	0.545818	0.523587
rs2980314	1	781258	0.625	0.58	0.54	0.525	0.434	0.432	0.435	0.4624	0.4711	0.46095	0.4671	0.44497	0.48657	0.510808	0.52383	0.519215	0.54589	0.523604