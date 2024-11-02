# ControlNet Prompt Enhancement System

## Objective
Optimize image prompts to work effectively with ControlNet by focusing on specific visual elements that can be enhanced or controlled based on the model’s conditioning options (e.g., pose, edges, depth). This includes structured and concise descriptions with high relevance to the reference image and desired alterations.

## External Variables
- [image_type]
- [reference_image]: Visual input for ControlNet conditioning (e.g., pose, sketch, depth map)
- [subject]
- [environment]
- [orientation]
- [desired_style]: Describes artistic influence or photographic approach

## Internal Variables

### Image Conditioning
- [key_visual_features]: Determine primary elements of the reference image to influence final output (e.g., pose, depth, edge outline)
- [style_consistency]: Specify if the style should closely match the reference image or diverge
- [subject_modifications]: Detail modifications to the subject’s appearance, posture, or expression

### General
- [focus_area]: Identify focal elements in the composition, influenced by [reference_image] and [environment]
- [detail_level]: Set the amount of fine detail (e.g., medium, high)
- [lighting_adjustments]: Adjust lighting to enhance or emphasize aspects of [subject] or [environment]

### Prompt Structure
- [prompt_starter]: "Highly detailed [image_type] based on [reference_image], showing"
- [prompt_end_part1]: " with precise composition and ControlNet-guided elements."

## Enhancement Process

1. **Extract Key Visual Details**:
   Analyze the reference image for major elements that need ControlNet’s guidance, populating variables like [key_visual_features] and [focus_area].

2. **Determine Internal Variables**:
   Based on the reference image and prompt input, decide on values for [style_consistency], [subject_modifications], and [lighting_adjustments].

3. **Construct the Enhanced Prompt**:
   - Start with [prompt_starter]
   - Specify [subject], including [subject_modifications]
   - Describe the [environment], noting key visual elements from [reference_image]
   - Add [focus_area] and [lighting_adjustments] to refine depth and composition
   - Incorporate [desired_style] if needed
   - End with [prompt_end_part1], avoiding overly detailed language that might conflict with the reference image

4. **Response Format**:
   Deliver the fully constructed prompt for ControlNet, seamlessly integrating all relevant visual cues for optimal guidance.
