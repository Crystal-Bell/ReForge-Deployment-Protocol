​An application that turns physical clutter or raw environmental debris into functional utility blueprints using computer vision and modular recipes.{
  "material_id": "MAT_PET_002",
  "name": "Polyethylene Terephthalate (PET) 2-Liter Bottle",
  "category": "Rigid Polymer",
  "physical_properties": {
    "state": "Solid",
    "density_g_cm3": 1.38,
    "melting_point_celsius": 250,
    "tensile_strength_mpa": 55,
    "rigidity_index": 0.75,
    "waterproof": true,
    "buoyancy": "High"
  },
  "chemical_behavior": {
    "combustibility": "Moderate (releases toxic fumes if unventilated)",
    "reactive_agents": ["Strong bases", "Ketones"],
    "thermal_shrinkage_temp_celsius": 80
  },
  "utility_affordances": [
    "Fluid containment / Hydration vessel",
    "Structural casing / Sleeve housing",
    "Buoyancy module / Floatation collar",
    "Thermal chimney / Air ducting"
  ]
}
App Architecture: Debris-to-Design Engine
An application that turns physical clutter or raw environmental debris into functional utility blueprints using computer vision and modular recipes.
1. Core Functional Loop
 * Capture: User snaps a photo of a room, garage, or yard pile.
 * Scan: Object-detection vision models identify physical items (e.g., plastic bottles, cardboard tubes, fabric scraps, dry grass, wax remnants).
 * Matrix Match: The system cross-references item properties against a database of upcycling and survival mechanics.
 * Synthesize: Generates an actionable build blueprint with step-by-step instructions.
2. System Workflow & Data Pipeline
| Pipeline Stage | Technology / Method | Function |
|---|---|---|
| Ingestion | Multimodal Vision API | Detects and bounds items in an image, tagging material types (plastic, paper, organic, metal). |
| Property Tagging | Material Metadata Schema | Assigns physical attributes (combustibility, tensile strength, liquid retention, rigidity). |
| Logic Engine | Rule-Based Matching Algorithm | Pairs raw materials with utility outputs (e.g., Cardboard Tube + Shredded Grass + Wax \rightarrow All-Weather Fire Starter). |
| Output UI | Markdown / Modular Card Layout | Renders clear, step-by-step build guides with safety notes and tool requirements. |
3. Example Blueprint Output
 * Detected Input: Cardboard toilet paper tubes, old candle wax remnants, dry lawn clippings.
 * Synthesized Utility: High-Efficiency Tinder Pod / Fire Starter.
 * Build Sequence:
   * Pack the interior of the cardboard tube tightly with dried grass and shredded paper.
   * Melt down residual wax fragments safely.
   * Pour molten wax evenly through the core matrix to bind the organic fuel.
   * Allow to cool, then segment into individual waterproof ignition pods.
Do you want to map out the material property database schema or the visual object-recognition prompt logic first?
# SYSTEM PROMPT: Debris-to-Design Vision Parser
> **Role:** Multimodal Upcycling Computer Vision Agent  
> **Input:** RGB Image Matrix (Kitchen, Yard, or Workshop clutter)  
> **Output Structured Data:** JSON Array of Detected Items with Material Vectors  
{
  "model": "vision-multimodal-engine-v4",
  "parameters": {
    "temperature": 0.1,
    "response_format": { "type": "json_object" }
  },
  "messages": [
    {
      "role": "system",
      "content": "Analyze the provided image of household or yard debris. Identify every physical item present. For each item, return a JSON object containing: item_name, estimated_quantity, material_composition, structural_state (rigid, flexible, shredded, liquid), and top 3 potential upcycling utility roles based on physical affordances."
    },
    {
      "role": "user",
      "content": [
        {
          "type": "image_url",
          "image_url": { "url": "data:image/jpeg;base64,{user_captured_image_bytes}" }
        }
      ]
    }
  ]
}
: "Build a full-stack web application with a camera upload feature. When an image is uploaded, use a vision API to detect household debris, match it against the material property database, and output a step-up utility blueprint card."​"Analyze the uploaded image of household or industrial waste. Identify the primary material composition (e.g., HDPE plastic, corrugated cardboard, aluminum, steel hardware). Map the detected object to its nearest structural category, estimate its dimensional scale, and list three potential upcycled utility applications based on its material rigidity and form factor."{
  "material_id": "hdpe_plastic_jug_gallon",
  "category": "Rigid Plastic",
  "tensile_strength": "Medium-Low",
  "load_bearing_capacity": "Non-structural / Enclosure or Panel",
  "cutting_tools_required": ["Utility Knife", "Tin Snips"],
  "joining_methods": ["Zip Ties", "Hot Glue", "Rivet Fasteners"],
  "common_sources": ["Milk jugs", "Laundry detergent containers"]
}
# ReForge-Deployment-Protocol