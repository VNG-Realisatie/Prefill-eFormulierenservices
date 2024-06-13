---
layout: page-with-side-nav
title: Documentatie Prefill eFormulierenservices
folder_files:
  - title: 2012 Persoonsgegevensverwerkingsprocessen (pdf)
    path: documenten/2012_Persoonsgegevensverwerkingsprocessen.pdf
    group: 10
    versie: 
    status: 
    omschrijving: 
    datum: 20141008
  - title: Koppelvlakspecificatie prefill eFormulieren - Berichtschema's (zip)
    path: documenten/20160201_PRS_102.zip
    group: 10
    versie: 1.0.2
    status: 
    omschrijving: 
    datum: 20160201
  - title: Koppelvlakspecificatie prefill eFormulieren Bijlage B (zip)
    path: documenten/Koppelvlakspecificatie_prefill_eFormulieren_Bijlage_B.xlsx.zip
    group: 10
    versie: 
    status: 
    omschrijving: 
    datum: 
  - title: Prefill eFormulierenservices v103 releasenotes (pdf)
    path: documenten/Prefill_eFormulierenservices_103_releasenotes.pdf
    group: 10
    versie: 1.0.3
    status: 
    omschrijving: 
    datum: 20170501
  - title: Specificatie Prefill E-formulierenservices v1.0.3 (pdf)
    path: documenten/Specificatie_Prefill_E-formulierenservices_v1.0.3.pdf
    group: 10
    versie: 1.0.3
    status: 
    omschrijving: 
    datum: 20170501
  - title: Testset prefill e-Formulieren 1.0 (zip)
    path: documenten/Testset_prefill_e-Formulieren_1.0.zip
    group: 10
    versie: 1.0
    status: Onbekend
    omschrijving: 
    datum: 20140702
---

# Documentatie

## Prefill eFormulierenservices 1.0

<table>
	<thead>
		<tr>
			<th>Document</th><th>Versie</th><th>Beheerstatus</th><th>Beschrijving</th><th>Versiedatum</th>
		</tr>
	</thead>
	<tbody>
		{% for i in page.folder_files %}
			{% if i.group == 10 %} 
				<tr>
					<td>
					  <a href="{{ i.path | base_url }}">
						{{ i.title }}
					  </a>
					</td>
					<td>{{ i.versie }}</td>
					<td>{{ i.status }}</td>
					<td>{{ i.omschrijving }}</td>
					<td>{{ i.datum }}</td>
				</tr>
			{% endif %} 
		{% endfor %}
	</tbody>
</table>
