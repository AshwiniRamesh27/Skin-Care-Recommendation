<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>💆‍♀️ AI-Powered Skin Care Recommendation System</title>
</head>
<body>

  <h1>💄 Simple Skin Care Recommendation Using Generative AI</h1>

  <p>
    <strong>simple_skin_care_recommendation.py</strong> is an AI-driven skincare assistant that combines 
    <strong>image understanding</strong>, <strong>few-shot prompting</strong>, and 
    <strong>retrieval-augmented generation (RAG)</strong> to generate personalized skincare recommendations 
    based on facial image analysis.  
    The system uses the <strong>Google Gemini API</strong> to analyze the user’s skin, detect concerns, 
    and recommend appropriate skincare routines using real product data from a Kaggle dataset.
  </p>

  <h2>🎯 Objective</h2>
  <p>
    To build an intelligent skincare recommendation system that:
  </p>
  <ul>
    <li>Analyzes facial skin type and conditions from an uploaded image.</li>
    <li>Retrieves relevant products from a skincare knowledge base using RAG.</li>
    <li>Generates an AM/PM skincare routine using few-shot prompting with Gemini.</li>
  </ul>

  <h2>🧠 Key Features</h2>
  <ul>
    <li><strong>Image Understanding:</strong> Detects skin type (oily, dry, sensitive) and concerns (acne, dullness, redness) using the Gemini Vision model.</li>
    <li><strong>RAG Integration:</strong> Retrieves product data from a Kaggle skincare dataset to ground the recommendations in real examples.</li>
    <li><strong>Few-Shot Prompting:</strong> Ensures consistent and structured skincare routines using prompt-based examples.</li>
    <li><strong>Personalization:</strong> Tailors skincare suggestions based on unique skin profiles.</li>
    <li><strong>Product Filtering:</strong> Dynamically filters the dataset to show only products matching the user's needs.</li>
  </ul>

  <h2>📁 Workflow</h2>
  <ol>
    <li><strong>Data Import:</strong> Downloads Kaggle dataset <code>taniadh/skin-care</code> for skincare product information.</li>
    <li><strong>Face Image Upload:</strong> User uploads an image through an interactive widget.</li>
    <li><strong>Skin Analysis:</strong> The Gemini model analyzes the image and produces a descriptive result with a simplified label (e.g., <em>dry-sensitive</em>).</li>
    <li><strong>Keyword Generation:</strong> Gemini extracts skincare-related keywords to guide product retrieval.</li>
    <li><strong>RAG Filtering:</strong> Filters the Kaggle dataset to find products that match the user’s concerns.</li>
    <li><strong>Few-Shot Prompting:</strong> Generates a complete skincare routine using both user analysis and retrieved product data.</li>
  </ol>

  <h2>🧩 Functions Overview</h2>
  <ul>
    <li><code>analyze_skin_image(image_bytes)</code> → Analyzes uploaded facial image and identifies skin type and issues.</li>
    <li><code>generate_keyword(description)</code> → Extracts relevant skincare keywords for dataset filtering.</li>
    <li><code>skin_care_recommendation(desc_result, retrieved_info)</code> → Generates personalized routine using Gemini and retrieved products.</li>
  </ul>

  <h2>📦 Dependencies</h2>
  <pre><code>
pip install google-genai==1.7.0 pandas ipywidgets kagglehub
  </code></pre>

  <h2>🚀 Run Instructions</h2>
  <pre><code>
    
# Step 1: Download Kaggle dataset 
import kagglehub
kagglehub.dataset_download('taniadh/skin-care')

# Step 2: Install required packages
!pip install -qU "google-genai==1.7.0"

# Step 3: Run script 
python simple_skin_care_recommendation.py
  </code></pre>

  <h2>📊 Example Workflow</h2>
  <ol>
    <li>User uploads an image of their face via widget.</li>
    <li>Gemini analyzes the skin and returns:
      <pre><code>Skin type: oily-acne prone. Issues: enlarged pores, oil buildup.</code></pre>
    </li>
    <li>Gemini extracts keywords like:
      <pre><code>acne|oily|hydrating|pore|oil-control</code></pre>
    </li>
    <li>System filters the product list and retrieves relevant items.</li>
    <li>Final recommendation generated:
      <pre><code>
Routine:
- Cleanser: Oil Control Gel Cleanser
- Toner: Some By Mi AHA BHA PHA
- Serum: Skintific 2% Salicylic Acid
- Moisturizer: Lightweight Gel Moisturizer
- Sunscreen: Azarine Hydrasoothe SPF 45
      </code></pre>
    </li>
  </ol>

  <h2>💡 AI Techniques Used</h2>
  <ul>
    <li><strong>Vision-Language Understanding:</strong> Gemini model processes facial images with text prompts.</li>
    <li><strong>Few-Shot Learning:</strong> Predefined skincare examples guide model responses for consistency.</li>
    <li><strong>Retrieval-Augmented Generation (RAG):</strong> Uses product dataset to ground the generated skincare recommendations.</li>
  </ul>

  <h2>🔒 Privacy & Ethical Considerations</h2>
  <ul>
    <li>Facial images are processed locally and not stored permanently.</li>
    <li>No user personal information is logged.</li>
    <li>Generated routines are for educational and experimental purposes, not medical diagnosis.</li>
  </ul>

  <h2>📊 Example Dataset Fields</h2>
  <pre><code>
product_type | product_name | product_brand | product_description
---------------------------------------------------------------------
Cleanser     | Oil Control Gel Cleanser | Some By Mi | Acne & pore care
Serum        | Hyaluronic Acid Booster | The Ordinary | Deep hydration serum
Moisturizer  | Water Bank Moisture Cream | Laneige | Suitable for dry skin
  </code></pre>

  <h2>🧠 Model Used</h2>
  <ul>
    <li><strong>Gemini 2.5 Flash Lite</strong> — for image analysis and text generation.</li>
    <li>Supports multimodal input (text + image).</li>
  </ul>

  <h2>🧾 Output</h2>
  <ul>
    <li><strong>Skin Analysis:</strong> Text-based summary of the user’s skin condition.</li>
    <li><strong>Keywords:</strong> List of attributes used for product filtering.</li>
    <li><strong>Final Recommendation:</strong> Personalized AM/PM skincare routine.</li>
  </ul>

  <h2>📧 Contact</h2>
  <p>
    <strong>Ashwini Ramesh</strong><br>
    📧 <a href="mailto:ashwiniramesh2709@gmail.com">ashwiniramesh2709@gmail.com</a><br>
    🔗 <a href="https://linkedin.com/in/ashwini27" target="_blank">LinkedIn</a>
  </p>

</body>
</html>
