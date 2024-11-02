# Enhanced Prompt for Conditioned Model

## Objective
Optimize image prompts to effectively incorporate the details and features of a given reference image, focusing on specific visual elements that can be enhanced or controlled based on the model’s conditioning options. This template provides a structured and concise description with high relevance to the reference image and any desired alterations.

## External Variables
- ["{user_prompt}"]: Describes the main subject or theme, provided by the user make sure to include this in the prompt
- [image_type]: Type of image to be generated (e.g., portrait, landscape, abstract)
- [reference_image]: Visual input used to guide the model's output (e.g., pose, sketch, depth map)
- [subject]: A general description of the main figure or focal element (e.g., person, object, scene)
- [environment]: Background or setting in which the subject is placed
- [orientation]: Orientation of the subject in the frame (e.g., full-body, close-up)
- [desired_style]: Describes the artistic influence or photographic approach (e.g., vintage, surreal, realistic)

## Internal Variables

### Visual Conditioning
- [key_visual_features]: Determine primary elements of the reference image that should influence the final output (e.g., pose, depth, edge outline)
- [style_consistency]: Specify if the style should closely match the reference image or diverge
- [subject_modifications]: Detail modifications to the subject’s appearance, posture, or expression to fit the user prompt

### General
- [focus_area]: Identify focal points in the composition, influenced by [reference_image] and [environment]
- [detail_level]: Set the level of detail desired (e.g., medium, high)
- [lighting_adjustments]: Adjust lighting to enhance or emphasize aspects of [subject] or [environment] as needed

### Prompt Structure
- [prompt_starter]: "Highly detailed [image_type] based on [reference_image], showing"
- [prompt_end_part1]: " with precise composition and elements guided by the reference image."

## Enhancement Process

1. **Extract Key Visual Details**:
   Analyze the reference image to identify major visual elements that will guide the model’s conditioning, populating variables such as [key_visual_features] and [focus_area].

2. **Determine Internal Variables**:
   Based on the reference image and the input from "{user_prompt}", assign values to [style_consistency], [subject_modifications], and [lighting_adjustments].

3. **Construct the Enhanced Prompt**:
   - Start with [prompt_starter]: "Highly detailed [image_type] based on [reference_image], showing"
   - Specify [subject] using general characteristics that align with "{user_prompt}" and [subject_modifications]
   - Describe the [environment], incorporating key visual elements identified from [reference_image]
   - Add [focus_area] and [lighting_adjustments] to enhance depth and overall composition
   - If relevant, include [desired_style] for stylistic consistency
   - Conclude with [prompt_end_part1], maintaining clarity and avoiding overly complex language that might conflict with the reference image

4. **Response Format**:
   Deliver the fully constructed prompt, seamlessly incorporating all relevant visual details from the reference image with the user prompt for optimal guidance and output.
