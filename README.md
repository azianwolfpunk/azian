# azian    
    Weld Plan Compiler Code Package v0.0.3               AS OF: 08FEB2019
    ------------------------------------
    ------------------------------------
   INDEX of README
    ---------------
    0-a.-INDEX of README
     -b.-INDEX of FOLDER
    1-   TERMINOLOGY
    2-   PROCESS and PLANNING
    
    
    INDEX of FOLDER
    ------------------
    0-Example Weld Plans
    1-Scripts
    2-Templates
    3-Weld Information
    
    --------------------------------------------------------------------------------------------------------------------------
    --------------------------------------------------------------------------------------------------------------------------
    
    1-TERMINOLOGY
    -------------
    IBI: Illinois Blower, INC
    
    Weld Descriptions: the IBI part number description- denoted by a "050-0XXX" number, containing weld type and callouts to weld procedures.
    
    WPS: Weld Procedure Specification- Procdeure for doing a weld, due to type and materials.
    
    PQR: Procedure Qualification Record- Certification of WPS by qualified inspector.
    
    NDE: Non Destructive Examination- Post-weld inspection reports due to type of inspection needed as requested by customer.
    
    PMI: Positive Material Inspection- Inspection reports of supplier material upon reception.
    
    P#: Type of material grouping for material types (i.e. P1 is Carbon Steel, P8 Stainless..)
    
    Weld Label:   ID stamped near weld callouts on drawing files- usually denoted by a flag with two letters paired inside (i.e. "AA" "BB"). 
       /Callout   ID's should be consistent throughout whole plan. Welds with the same weld type, or description, on different materials will get different labels.
    
    WIR: Weld Inspection Record- Report that contains all weld callouts/Labels/ID's with respective part numbers, WPS and PQR overviews, NDE callouts, and PMI information.
    
    "-W': Weldment Drawing- CAD PDF drawing with omitted dimensions to emphasize weld callouts.
    
    Weld Plan: The "pre-weld" quality plan submitted for approval, revised -if needed, and followed.
    	Should include:
    	Cover sheets
    	Index
    	Weld Descriptions of welds used
    	WIR's (WIR)
    	   Insepctions needed
    	   Weldment Drawings	
    	WPS's
    	   PQR's
    	[Misc. Weld Documents TBD]
    	
    --------------------------------------------------------------------------------------------------------------------------
    --------------------------------------------------------------------------------------------------------------------------
    
    2-PROCESS and PLANNING
    ----------------------
    Currently:
    	Fixes openpyxl from merged cell border style issue
    	Basic GUI for data input
    	Creates an Excel WIR file for each part
    	Lists all welds in WIR for each part
    	Create new folder file paths per Sales Order
    	Creates coversheets/index with customer info
    
    In process:
    	List all parts with repective weld information on coversheet
    		-needs to append data from weld loop, to cover sheet
    	Cataloging all required data for "API" callout
    Needs:
    	Either:
    		-Rolling code callouts for weld labels (assign weld type, due to materials, a label and standardize that across the assembly)- ID's would be different across different jobs, but consistent within job
    		or
    		-Standardize all weld desciptions due to each material with weld labels- would take a while to catalog a database for information
    
    	Solidworks API streamlining- be able to have assemblies package every weld listed and properly label weld and automatically pull part info
    		(Would need weld symbol knowledge and disipline with designers, and learning a Python Solidworks workthrough)
    		Ideal to also have dimensions on layer so a macro could hide dimension layer to leave weld callouts on drawing for "-W" drawings.
    		(would need designer disipline and could possible eliminate this step)
    
    	Choosing template destination/directory (whether it's manual or with package installer)
    
    	Choose save destination (has static file path, with input based path creation, but ideal to have GUI for save destination)
    
    	See previous weld packages for editing
    	
    	File search and copier to find, due to weld type and material, respective "-W", WPS, PQR, and NDE PDF's
