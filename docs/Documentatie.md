---
layout: page-with-side-nav
title: Documentatie Prefill eFormulierenservices
folder_files:
  - title: 2012 Persoonsgegevensverwerkingsprocessen
    path: documenten/2012_Persoonsgegevensverwerkingsprocessen.pdf
    group: 10
    versie: 
    status: 
    omschrijving: 
  - title: Addendum Prefill 0
    path: documenten/Addendum_Prefill_0.pdf
    group: 10
    versie: 
    status: 
    omschrijving: 
  - title: Koppelvlakspecificatie prefill eFormulieren - Berichtschema's 
    path: documenten/20160201_PRS_102.zip
    group: 10
    versie: 1.0.2
    status: 
    omschrijving: 
  - title: Koppelvlakspecificatie prefill eFormulieren Bijlage B 
    path: documenten/Koppelvlakspecificatie_prefill_eFormulieren_Bijlage_B.xlsx.zip
    group: 10
    versie: 
    status: 
    omschrijving: 
  - title: Prefill eFormulierenservices v103 releasenotes 
    path: documenten/Prefill_eFormulierenservices_103_releasenotes.pdf
    group: 10
    versie: 1.0.3
    status: 
    omschrijving: 
  - title: Specificatie Prefill E-formulierenservices v1.0.3 
    path: documenten/Specificatie_Prefill_E-formulierenservices_v1.0.3.pdf
    group: 10
    versie: 1.0.3
    status: 
    omschrijving: 
  - title: Testset prefill e-Formulieren 1.0
    path: documenten/Testset_prefill_e-Formulieren_1.0.zip
    group: 10
    versie: 1.0
    status: Onbekend
    omschrijving: 
---

# Documentatie

## Prefill eFormulierenservices 1.0

<table>
	<thead>
		<tr>
			<th>Document</th><th>Versie</th><th>Beheerstatus</th><th>Beschrijving</th>
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
				</tr>
			{% endif %} 
		{% endfor %}
	</tbody>
</table>
