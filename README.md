Why GIS is crucial:
It helps understand risks spatially (like floods, droughts, or infrastructure exposure).
It enables smarter decisions about development, disaster response, and climate adaptation.
And most importantly — GIS transforms data into action.

GISCI Webinars – Free educational webinars and resources to help you with professional development in GIS and project management
🌐 Explore GISCI
NASA Earth Science Data Management Course – Free course on Earth science, remote sensing, and space data management
🌐 Explore NASA Earth Science
USGIF GEOINT Certificate (Free Introductory Course) – Start learning geospatial intelligence with free resources from the USGIF
🌐 Explore USGIF GEOINT
OpenGIS – Free open-source tools and tutorials for geospatial and remote sensing project management
🌐 Explore OpenGIS
Esri Free Learning – Learn ArcGIS and geospatial data management with free resources
🌐 Explore Esri Academy

California Utilities (LADWP, PG&E, SCE, SDG&E, SMUD
----

BA worked 176 hours in July month. Requesting to kindly approve below timesheet ASAP.

Request Number - 3992711

SELECT SPLIT_PART(unique_sitepolygon_id, '_', 2) as project_id, COUNT(*) as duplicates, STRING_AGG(unique_sitepolygon_id, ', ') as ids FROM shug.ept_sitepolygon_evw WHERE unique_sitepolygon_id LIKE 'SP_%' GROUP BY 1 HAVING COUNT(*) > 1 ORDER BY MAX(ept_last_edited) DESC;

SELECT unique_sitepolygon_id, COUNT(*) FROM shug.ept_sitepolygon_evw GROUP BY unique_sitepolygon_id HAVING COUNT(*) > 1;

SELECT * FROM shug.ept_projects WHERE unique_project_id IN (SELECT unique_project_id FROM shug.ept_projects GROUP BY unique_project_id HAVING COUNT(*) > 1);

SELECT SPLIT_PART(unique_sitepolygon_id, '_', 2) as project_id, COUNT(*), STRING_AGG(unique_sitepolygon_id, ', ') as all_ids FROM shug.ept_sitepolygon_evw WHERE unique_sitepolygon_id LIKE 'SP_%' GROUP BY 1 HAVING COUNT(*) > 1;

SELECT * FROM shug.ept_sitepolygon_evw WHERE unique_sitepolygon_id IN (SELECT unique_sitepolygon_id FROM shug.ept_sitepolygon_evw GROUP BY unique_sitepolygon_id HAVING COUNT(*) > 1) ORDER BY unique_sitepolygon_id;

SELECT unique_sitepolygon_id, pm_id, created FROM shug.ept_sitepolygon_evw WHERE SPLIT_PART(unique_sitepolygon_id, '_', 2) IN (SELECT SPLIT_PART(unique_sitepolygon_id, '_', 2) FROM shug.ept_sitepolygon_evw WHERE unique_sitepolygon_id LIKE 'SP_%' GROUP BY SPLIT_PART(unique_sitepolygon_id, '_', 2) HAVING COUNT(*) > 1) ORDER BY SPLIT_PART(unique_sitepolygon_id, '_', 2), unique_sitepolygon_id;

SELECT SPLIT_PART(unique_sitepolygon_id, '_', 2) as project_id, COUNT(*), STRING_AGG(unique_sitepolygon_id, ', ') as all_ids FROM shug.ept_sitepolygon_evw WHERE unique_sitepolygon_id LIKE 'SP_%' GROUP BY 1 HAVING COUNT(*) > 1;

SELECT * FROM shug.ept_sitepolygon_evw WHERE SUBSTRING(unique_sitepolygon_id,4,8) IN (SELECT SUBSTRING(unique_sitepolygon_id,4,8) FROM shug.ept_sitepolygon_evw WHERE unique_sitepolygon_id LIKE 'SP_%' GROUP BY SUBSTRING(unique_sitepolygon_id,4,8) HAVING COUNT(*)>1) ORDER BY SUBSTRING(unique_sitepolygon_id,4,8);

SELECT COUNT(*) FROM shug.ept_sitepolygon_evw WHERE unique_sitepolygon_id LIKE 'SP_%';
