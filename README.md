# capad-ont
Loc-I conformant Ontology for Collaborative Australian Protected Areas

The data structure is described in the catalogue entry: http://www.environment.gov.au/fed/catalog/search/resource/details.page?uuid=%7BAF4EE98E-7F09-4172-B95E-067AB8FA10FC%7D 

> The main attributes of Marine CAPAD 2018 are described below. For more information please refer to the CAPAD Technical Specification document.

> Marine CAPAD 2018 Attributes:

PA_ID: A unique three digit code for the protected area that should persist between versions of CAPAD. This field was named 'PA_ID_grp' in CAPAD 2016.

PA_PID: A unique code for a parcel or zone within a protected area that should persist between versions of CAPAD. The first three digits of the PA_PID code (the PA_ID) are common to all component polygons of a single protected area. This field was named 'PA_ID' in previous versions of CAPAD.

NAME: The official (gazetted) name of a protected area.

TYPE: The type of protected area according to the establishment mechanism. e.g. Marine National Park, Marine Sanctuary, Indigenous Protected Area

TYPE_ABBR: The abbreviation of the protected area TYPE.
AMP = Australian Marine Park
AQR = Aquatic Reserve
CA = Conservation Area
CP = Conservation Park
DPAA = Dugong Protection Area (A)
DPAB = Dugong Protection Area (B)
DS = Dolphin Sanctuary
FHAA = Fish Habitat Area (A)
FHAB = Fish Habitat Area (B)
FHPA = Fish Habitat Protection Area
GR = Game Reserve
IPA = Indigenous Protected Area
LS = Rock Lobster Sanctuary
MCA = Marine Conservation Area
MMA = Marine Management Area
MNP = Marine National Park
MNR = Marine Nature Reserve
MP = Marine Park
MS = Marine Sanctuary
NP = National Park
NPC = National Park (Commonwealth)
NPS4 = National Parks Act - Schedule 4 park or reserve
NR = Nature Reserve
S5G = 5(1)(g) Reserve
S5H = 5(1)(h) Reserve
SH = Shipwreck Reserve

IUCN: the IUCN protected area management category ascribed by the managing authority.
IA = Strict Nature Reserve
IB = Wilderness Area
II = National Park
III = Natural Monument or Feature
IV = Habitat/Species Management Area
V = Protected Landscape/Seascape
VI = Protected area with sustainable use of natural resources
NR = (Not Reported) - For protected areas where an IUCN category is unknown and/or the data provider has not provided any related information.
NA = (Not Applicable) - Denotes an area that does not meet the NRS criteria or the IUCN definition of a protected area but has management complimentary to the NRS.
NAS = (Not Assigned) - The protected area meets the standard definition of protected areas but the data provider has chosen not to use the IUCN Protected Area Management Categories.


NRS_MPA: This attribute indicates the status of the protected area in terms of meeting the standard for inclusion in the NRSMPA. For marine reserves refer to the document “Guidelines for Establishing the National Representative System of Marine Protected Areas (NRSMPA)
Y = Yes. The sea has been assessed as a protected area that meets the standard for inclusion in the NRSMPA.
N = No. The sea has been assessed as not meeting the standard for inclusion in the NRSMPA. It is managed for nature conservation without meeting the NRSMPA standard.
ND = Not Determined. The sea is managed for nature conservation although it has not been assessed to determine if it meets the standard for inclusion in the NRSMPA.

Note that for the calculation of area statistics only protected areas with an NRS_PA value of 'Y' or 'I' are included.


GAZ_AREA: area in hectares as described in the nomination document (e.g. parliamentary gazettal), to the nearest hectare. Some protected areas do not have a specific area in the designation.

GIS_AREA: The area of a protected area based on current spatial data in the Albers Equal Area projection calculated by DoEE using ArcGIS software. It is this field that is used to calculate the statistics provided in spreadsheets at: www.environment.gov.au/capad/

GAZ_DATE: Gazettal date of the original proclamation that established any form of protected area.

LATEST_GAZ: The date of the most recent gazettal or proclamation to amend the protected area. It can be the same as the GAZ_DATE if there have been no changes or additions to the protected area.

STATE: The CODE for the State or Territory in which the Protected Area is located. Marine Commonwealth managed protected areas are attributed with the name of 'COM' as they are generally within Commonwealth waters. EXT= protected areas located in Australian external territories.

AUTHORITY: The CODE for the authority that manages the Protected Area.
DOEE = Australian Government, Department of the Environment and Energy
GBRMPA = Great Barrier Reef Marine Park Authority
IMG = Indigenous Management Group
LILC = Local Indigenous Land Council
NSW_DPI = NSW Department of Primary Industries
NT_PWCNT= Parks and Wildlife Commission of the NT
PIRSA = Primary Industries and Regions South Australia
QLD_DAF = Queensland Department of Agriculture and Fisheries
QLD_DES = Queensland Department of Environment and Science
SA_DEW = South Australian Department for Environment and Water
TAS_DPIPWE = Tasmanian Department of Primary Industries, Parks, Water and Environment
TSRA = Torres Strait Regional Authority
VIC_DELWP = Victorian Department of Environment, Land, Water and Planning
WA_DBCA = Western Australian Department of Biodiversity, Conservation and Attractions
WA_DPIRD = Western Australian Department of Primary Industries and Regional Development


DATASOURCE: The CODE for the agency which supplied the Protected Area data.
DOEE = Australian Government Department of the Environment and Energy
GBRMPA = Great Barrier Reef Marine Park Authority
NSW_DPI = NSW Department of Primary Industries
NT_PWCNT= Parks and Wildlife Commission of the NT
PIRSA = Primary Industries and Regions South Australia
QLD_DAF = Queensland Department of Agriculture and Fisheries
QLD_DES = Queensland Department of Environment and Science
SA_DEW = South Australian Department of Environment and Water
TAS_DPIPWE = Tasmanian Department of Primary Industries, Parks, Water and Environment
TSRA = Torres Strait Regional Authority
VIC_DELWP = Victorian Department of Environment, Land, Water and Planning
WA_DBCA = Western Australian Department of Biodiversity, Conservation and Attractions
WA_DPIRD = Western Australian Department of Primary Industries and Regional Development


GOVERNANCE: The CODE for the type of governance which has management and decision making responsibility.
C = Community - Community conserved areas where indigenous peoples or local communities (settled or mobile) hold decision-making authority, responsibility and accountability.
G = Government - Protected areas with decision-making authority, responsibility and accountability in the hands of national, state or local government
J = Joint - Jointly managed protected areas where several social actors from different governance types share decision-making authority, responsibility and accountability. Joint management arrangements are recognised by a management board, agreement (e.g. ILUA) or other formal arrangement.
P = Private - Private protected areas where land and resource owners hold decision-making authority, responsibility and accountability.

COMMENTS: Extra information jurisdictions elect to supply. Due to the change in ENVIRON based categorisation rules in the 2016/2018 versions of CAPAD, it has been noted in the COMMENTS field of marine CAPAD if a record was previously included in terrestrial CAPAD.

ENVIRON: The code denotes the environment type conserved in the protected area as described by the data custodian. A protected area can assigned an ENVIRON value of terrestrial, marine or both.
T = Terrestrial - Generally includes land and or water above high water mark including aquatic ecosystems.
B = Both - Includes land and water both above and below the high water mark.
M = Marine - Generally includes land and or water below high water mark and may include islands and reefs above high water mark.

Terrestrial CAPAD contains 'T' and 'B' protected areas. Marine CAPAD contains 'M' and 'B' protected areas. If a protected area is coded as 'B' by the data provider, DoEE calculates the proportional representation of marine and terrestrial areas within the protected area (all component polygons combined). If 70% or more of the protected area is marine then the whole protected area is included in the marine CAPAD dataset. If less than 70% protected area is marine then the whole protected area is included in the terrestrial CAPAD dataset.
Prior to CAPAD 2016 only ENVIRON ='M' records were included in Marine CAPAD, all ENVIRON = 'T' or 'B' records were included in Terrestrial CAPAD. The method described above for managing ENVIRON = 'B' areas was introduced in CAPAD 2016 (and revised slightly in CAPAD 2018).

MGT_PLAN: The CODE for the status of the management plan for the protected area.
P = In Preparation - Some form of management document was being prepared.
D = Draft - A draft management document was released for comment by the public, management board or equivalent.
S = Statutory - Enabling legislation establishes the management of a protected area and separate management document is not required.
I = Management Intent - A formal statement of management intent has been prepared that clearly sets out the management objectives for the protected area but includes little else.
M = Management Plan - A formally adopted management plan that has been through consultation and contains strategies and actions for implementation for this protected area.
R = Regional Plan - A formally adopted management plan has been through consultation and contains general strategies and actions for implementation over a group of protected areas.
N = Unknown - No form of management document could be found.
UR = Under Review - The management plan is under review

RES_NUMBER: The reserve number (if declared) as used by the controlling authority. IPA Reserve numbers are allocated by DoEE.

ZONE_TYPE: This is a concatenation of the ZONE (usually found in the COMMENTS field) and IUCN categories – for use when mapping the reserves.

EPBC: This identifies if the reserve can be considered under the Commonwealth Environment Protection and Biodiversity Conservation Act 1999 (EPBC Act).
Commonwealth = Commonwealth reserve (either a Commonwealth Marine Reserve, Marine Park, Marine Sanctuary, National Park (Commonwealth)) – as outlined in Section 342 of the Act.
State = State managed reserve – as supplied by State/Territory authority

LONGITUDE: Longitude coordinate of polygon centroid in decimal degrees, derived by DoEE from Geographics projected dataset.

LATITUDE: Latitude coordinate of polygon centroid in decimal degrees, derived by DoEE from Geographics projected dataset.

