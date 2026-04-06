---
title: Research
nav:
  order: 1
  tooltip: Published works
---

<style>
.research-overview {
  display: flex;
  flex-direction: column;
  gap: 1.4rem;
}

.research-lead-card,
.research-section-card {
  position: relative;
  overflow: hidden;
  border: 1px solid rgba(0, 39, 76, 0.14);
  background:
    radial-gradient(circle at top right, rgba(255, 203, 5, 0.12), transparent 32%),
    linear-gradient(180deg, rgba(255, 255, 255, 0.96), rgba(246, 249, 252, 0.96));
  border-radius: calc(var(--rounded) + 2px);
  box-shadow: 0 20px 45px rgba(10, 30, 55, 0.08);
  padding: 1.25rem 1.35rem;
}

.research-lead-card::before,
.research-section-card::before {
  content: "";
  position: absolute;
  inset: 0 auto auto 0;
  width: 100%;
  height: 4px;
  background: linear-gradient(90deg, #00274c, #005f91, #ffcb05);
}

.research-lead-card h2,
.research-section-card h2 {
  margin-top: 0;
  margin-bottom: 0.7rem;
  border-bottom: none;
  padding-bottom: 0;
}

.research-lead {
  margin: 0 0 0.85rem;
  line-height: 1.6;
  font-size: 1.02rem;
}

.research-topic-nav {
  display: grid;
  grid-template-columns: 1fr;
  gap: 1.05rem;
}

.research-topic-nav-group {
  position: relative;
  border: 1px solid rgba(0, 39, 76, 0.12);
  background:
    linear-gradient(180deg, rgba(255, 255, 255, 0.92), rgba(242, 247, 251, 0.94));
  border-radius: 16px;
  padding: 1rem 1.05rem 0.95rem;
  box-shadow: 0 14px 30px rgba(10, 30, 55, 0.06);
}

.research-topic-nav-group::after {
  content: "";
  position: absolute;
  right: -24px;
  top: -24px;
  width: 90px;
  height: 90px;
  border-radius: 999px;
  background: radial-gradient(circle, rgba(0, 39, 76, 0.1), transparent 68%);
  pointer-events: none;
}

.research-topic-nav-link {
  display: block;
  font-family: var(--heading);
  font-weight: 800;
  margin-bottom: 0.65rem;
  text-decoration: none;
  font-size: 1rem;
  line-height: 1.35;
  color: #00274c;
}

.research-topic-nav-sublinks {
  margin: 0;
  padding-left: 1.1rem;
}

.research-topic-nav-sublinks li {
  margin: 0.35rem 0;
  padding-left: 0;
  text-align: left;
}

.research-topic-nav-sublinks li > a:first-child {
  font-weight: 800;
  color: #0b4f7c;
  text-decoration: none;
}

.research-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 1.1rem;
}

.research-topic-card {
  display: grid;
  grid-template-columns: minmax(0, 1.92fr) minmax(178px, 0.68fr);
  gap: 1rem;
  border: 1px solid rgba(0, 39, 76, 0.12);
  background:
    linear-gradient(180deg, rgba(255, 255, 255, 0.95), rgba(245, 248, 252, 0.95));
  border-radius: 18px;
  padding: 1rem;
  box-shadow: 0 16px 34px rgba(10, 30, 55, 0.07);
.research-topic-title {
  grid-column: 1 / -1;
  margin-top: 0;
  margin-bottom: 0.55rem;
  padding: 0.22rem 0 0.22rem 0.72rem;
  border-left: 4px solid #ffcb05;
  font-size: 1.06rem;
  line-height: 1.24;
  color: #0b4f7c;
  letter-spacing: 0.01em;
  text-transform: none;
  background: linear-gradient(90deg, rgba(0, 39, 76, 0.06), transparent 92%);
  border-radius: 0 10px 10px 0;
}

.research-topic-copy p {
  margin: 0 0 0.55rem;
  line-height: 1.5;
}

.research-topic-copy ul,
.research-topic-links ul {
  margin: 0;
  padding-left: 1.1rem;
}

.research-topic-copy li,
.research-topic-links li {
  margin: 0.28rem 0;
  padding-left: 0;
  text-align: left;
}

.research-topic-media {
  display: flex;
  align-items: center;
  justify-content: center;
}

.research-topic-media a {
  display: block;
  width: 100%;
}

.research-topic-media img,
.research-topic-placeholder {
  width: 100%;
  height: 220px;
  object-fit: contain;
  border-radius: 14px;
  border: 1px solid rgba(0, 39, 76, 0.12);
  background:
    linear-gradient(135deg, rgba(0, 39, 76, 0.14), rgba(255, 203, 5, 0.16));
  box-shadow: inset 0 0 0 1px rgba(255, 255, 255, 0.22);
}

.research-topic-placeholder {
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: var(--heading);
  font-weight: 800;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--primary);
}

.research-topic-links {
  grid-column: 1 / -1;
  border-top: 1px solid rgba(0, 39, 76, 0.1);
  padding-top: 0.8rem;
}

.research-topic-links h4 {
  margin: 0 0 0.45rem;
  font-size: 0.96rem;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  color: #00274c;
}

.research-paper-note {
  color: var(--gray);
}

.research-pub-strong {
  font-weight: 800;
  color: #00274c;
}

.research-topic-copy li::marker,
.research-topic-links li::marker,
.research-topic-nav-sublinks li::marker {
  color: #005f91;
}

.research-topic-card:hover,
.research-topic-nav-group:hover,
.research-lead-card:hover,
.research-section-card:hover {
  transform: translateY(-2px);
}

[data-dark="true"] .research-lead-card,
[data-dark="true"] .research-section-card,
[data-dark="true"] .research-topic-card,
[data-dark="true"] .research-topic-nav-group {
  background:
    radial-gradient(circle at top right, rgba(255, 203, 5, 0.08), transparent 32%),
    linear-gradient(180deg, rgba(7, 24, 40, 0.96), rgba(10, 28, 46, 0.96));
  border-color: rgba(120, 182, 255, 0.16);
}

[data-dark="true"] .research-topic-nav-link,
[data-dark="true"] .research-topic-links h4,
[data-dark="true"] .research-pub-strong {
  color: #ffde66;
}

[data-dark="true"] .research-topic-nav-sublinks li > a:first-child {
  color: #8ed8ff;
}

[data-dark="true"] .research-topic-title {
  color: #8ed8ff;
  background: linear-gradient(90deg, rgba(142, 216, 255, 0.12), transparent 92%);
  border-left-color: #ffde66;
}

[data-dark="true"] .research-topic-media img,
[data-dark="true"] .research-topic-placeholder {
  border-color: rgba(120, 182, 255, 0.18);
  background:
    linear-gradient(135deg, rgba(14, 79, 126, 0.28), rgba(255, 203, 5, 0.12));
}

@media (max-width: 950px) {
  .research-topic-nav,
  .research-grid,
  .research-topic-card {
    grid-template-columns: 1fr;
  }
}
</style>

<script>
document.addEventListener("DOMContentLoaded", function () {
  var gifImages = document.querySelectorAll('.research-topic-media img[src$=".gif"]');
  if (!gifImages.length) return;

  function replayGif(img) {
    var src = img.getAttribute("src");
    if (!src) return;
    var clean = src.split("?")[0];
    img.setAttribute("src", clean + "?r=" + Date.now());
  }

  if ("IntersectionObserver" in window) {
    var observer = new IntersectionObserver(function (entries) {
      entries.forEach(function (entry) {
        if (entry.isIntersecting) replayGif(entry.target);
      });
    }, { threshold: 0.55 });

    gifImages.forEach(function (img) {
      observer.observe(img);
      img.addEventListener("mouseenter", function () {
        replayGif(img);
      });
    });
  } else {
    gifImages.forEach(function (img) {
      img.addEventListener("mouseenter", function () {
        replayGif(img);
      });
    });
  }
});
</script>

# {% include icon.html icon="fa-solid fa-microscope" %}Research

<div class="research-overview">
  <section class="research-lead-card">
    <h2>Ongoing Research Projects</h2>
    <p class="research-lead">
      The lab studies how mobile, wearable, robotic, and IoT platforms can be turned into practical computational sensing systems that are more perceptive, more adaptive, and more useful in everyday environments.
    </p>

    <div class="research-topic-nav">
      <div class="research-topic-nav-group">
        <a class="research-topic-nav-link" href="#multimodal-projects">New Multi-modal Computational Sensing Technologies for Diverse Applications</a>
        <ul class="research-topic-nav-sublinks">
          <li><a href="#env-dynamics-project">Computational Sensing of Invisible Environmental Dynamics</a>: <a href="https://ambient-intelligence-lab-umich-eecs.github.io/MoireLens-Page/">MoiréLens</a> [<span class="research-pub-strong">SenSys'26</span>], <a href="{{ "/projects/" | relative_url }}?search=SoilNutri">SoilNutri</a> [<span class="research-pub-strong">UbiComp'26</span>], <a href="{{ "/projects/" | relative_url }}?search=VECTOR">VECTOR</a> [<span class="research-pub-strong">UbiComp'22</span>]</li>
          <li><a href="#health-wearables-project">Health Sensing using Wearable Consumer Electronics</a>: <a href="https://www.youtube.com/watch?v=FrSbxhM5yII">EarCardio</a> [<span class="research-pub-strong">MobiCom'26</span>], <a href="{{ "/projects/" | relative_url }}?search=EgoADL">EgoADL</a> [<span class="research-pub-strong">UbiComp'24</span>], <a href="{{ "/projects/" | relative_url }}?search=LoEar">LoEar</a> [<span class="research-pub-strong">UbiComp'22</span>]</li>
          <li><a href="#activity-reasoning-project">Fine-grained Human Activity Sensing and Reasoning</a>: <a href="https://github.com/leeyadong/UltraPoser">UltraPoser</a> [<span class="research-pub-strong">UIST'25</span>], <a href="{{ "/projects/" | relative_url }}?search=EgoADL">EgoADL</a> [<span class="research-pub-strong">UbiComp'24</span>]</li>
          <li><a href="#tactile-robotics-project">Tactile Sensing and Actuation for Robotics</a>: In submission</li>
        </ul>
      </div>

      <div class="research-topic-nav-group">
        <a class="research-topic-nav-link" href="#ai-native-projects">AI-Native Sensing Systems Challenges for Mobile, Wearable, Robotic, and IoT Platforms</a>
        <ul class="research-topic-nav-sublinks">
          <li><a href="#ai-optimization-project">AI-Assisted Mobile System Optimization</a>: <a href="{{ "/projects/" | relative_url }}?search=KDC">KDC</a> [<span class="research-pub-strong">NSDI'26</span>], <a href="{{ "/projects/" | relative_url }}?search=RFCanvas">RFCanvas</a> [<span class="research-pub-strong">SenSys'24</span>]</li>
          <li><a href="#secure-sensing-project">AI-Native Secure and Privacy-Preserving Sensing</a>: <a href="https://www.youtube.com/watch?v=Vgy-u9HlQOo">MagicPatch</a> [<span class="research-pub-strong">MobiCom'26</span>], <a href="{{ "/projects/" | relative_url }}?search=EveGuard">EveGuard</a> [<span class="research-pub-strong">S&amp;P'25</span>], <a href="{{ "/projects/" | relative_url }}?search=Magmaw">Magmaw</a> [<span class="research-pub-strong">NDSS'25</span>]</li>
          <li><a href="#native-ai-mobile-project">Sensing-Assisted Native AI Mobile System</a>: In submission</li>
          <li><a href="#ai-mobile-sensing-project">AI-Assisted Mobile Sensing System</a>: Ongoing</li>
          <li><a href="#wearable-memory-project">Wearable Agentic AI Memory System</a>: Ongoing</li>
        </ul>
      </div>
    </div>
  </section>

  <section class="research-section-card" id="multimodal-projects">
    <h2>New Multi-modal Computational Sensing Technologies for Diverse Applications</h2>

    <div class="research-grid">
      <article class="research-topic-card" id="env-dynamics-project">
        <h3 class="research-topic-title">Computational Sensing of Invisible Environmental Dynamics with Off-the-Shelf Sensors</h3>
        <div class="research-topic-copy">
          <p>We develop sensing systems that reveal environmental phenomena that are difficult for people and sensors to directly perceive in everyday settings.</p>
          <ul>
            <li>Repurposing commodity sensors to capture subtle airflow, temperature-field, and soil-state changes.</li>
            <li>Turning low-cost platforms into deployable tools for environmental understanding in real-world scenarios.</li>
          </ul>
        </div>
        <div class="research-topic-media">
          <a href="https://ambient-intelligence-lab-umich-eecs.github.io/MoireLens-Page/" target="_blank">
            <img src="{{ "images/moirelens.gif" | relative_url }}" alt="MoiréLens preview">
          </a>
        </div>
        <div class="research-topic-links">
          <h4>Selected Publications</h4>
          <ul>
            <li><a href="https://ambient-intelligence-lab-umich-eecs.github.io/MoireLens-Page/">MoiréLens</a> [<span class="research-pub-strong">SenSys'26</span>] <span class="research-paper-note">invisible airflow sensing using Moiré patterns</span></li>
            <li><a href="{{ "/projects/" | relative_url }}?search=SoilNutri">SoilNutri</a> [<span class="research-pub-strong">UbiComp'26</span>] <span class="research-paper-note">batteryless soil moisture and nitrogen sensing using UWB</span></li>
            <li><a href="{{ "/projects/" | relative_url }}?search=VECTOR">VECTOR</a> [<span class="research-pub-strong">UbiComp'22</span>] <span class="research-paper-note">temperature-field monitoring using acoustic signals</span></li>
          </ul>
        </div>
      </article>

      <article class="research-topic-card" id="health-wearables-project">
        <h3 class="research-topic-title">Health Sensing using Wearable Consumer Electronics</h3>
        <div class="research-topic-copy">
          <p>We build practical health sensing systems on consumer wearables and mobile devices for robust monitoring in everyday environments.</p>
          <ul>
            <li>Repurposing earbuds, phones, and lightweight wearable platforms for continuous physiological and behavioral sensing.</li>
            <li>Designing sensing pipelines that remain robust under motion, sparse sensing, and real-world deployment constraints.</li>
          </ul>
        </div>
        <div class="research-topic-media">
          <a href="https://www.youtube.com/watch?v=FrSbxhM5yII" target="_blank">
            <img src="{{ "images/earcardio.gif" | relative_url }}" alt="EarCardio preview">
          </a>
        </div>
        <div class="research-topic-links">
          <h4>Selected Publications</h4>
          <ul>
            <li><a href="https://www.youtube.com/watch?v=FrSbxhM5yII">EarCardio</a> [<span class="research-pub-strong">MobiCom'26</span>] <span class="research-paper-note">cardiac monitoring using commercial wireless earbuds</span></li>
            <li><a href="{{ "/projects/" | relative_url }}?search=LoEar">LoEar</a> [<span class="research-pub-strong">UbiComp'22</span>] <span class="research-paper-note">long-range contactless vital sign monitoring using acoustics</span></li>
          </ul>
        </div>
      </article>

      <article class="research-topic-card" id="activity-reasoning-project">
        <h3 class="research-topic-title">Fine-grained Human Activity Sensing and Reasoning in Ambient Environments</h3>
        <div class="research-topic-copy">
          <p>We study how ambient and wearable sensing systems can capture fine-grained human activities and support higher-level reasoning about daily behaviors in real-world environments.</p>
          <ul>
            <li>Combining multi-modal sensing for detailed activity understanding across body movement, context, and daily-life interactions.</li>
            <li>Building sensing pipelines that support both precise recognition and richer behavioral reasoning.</li>
          </ul>
        </div>
        <div class="research-topic-media">
          <a href="https://github.com/leeyadong/UltraPoser" target="_blank">
            <img src="{{ "images/25UIST_ultraposer.gif" | relative_url }}" alt="UltraPoser preview">
          </a>
        </div>
        <div class="research-topic-links">
          <h4>Selected Publications</h4>
          <ul>
            <li><a href="https://github.com/leeyadong/UltraPoser">UltraPoser</a> [<span class="research-pub-strong">UIST'25</span>] <span class="research-paper-note">full-body pose estimation using distributed wearables</span></li>
            <li><a href="{{ "/projects/" | relative_url }}?search=EgoADL">EgoADL</a> [<span class="research-pub-strong">UbiComp'24</span>] <span class="research-paper-note">multimodal daily-life logging using smartphone</span></li>
          </ul>
        </div>
      </article>

      <article class="research-topic-card" id="tactile-robotics-project">
        <h3 class="research-topic-title">Tactile Sensing and Actuation for Robotics</h3>
        <div class="research-topic-copy">
          <p>This direction explores how low-cost sensing and actuation pipelines can give robots richer tactile perception and more practical interaction capabilities.</p>
        </div>
        <div class="research-topic-media">
          <div class="research-topic-placeholder">In Submission</div>
        </div>
        <div class="research-topic-links">
          <h4>Selected Publications</h4>
          <ul>
            <li>In submission works</li>
          </ul>
        </div>
      </article>
    </div>
  </section>

  <section class="research-section-card" id="ai-native-projects">
    <h2>AI-Native Sensing Systems Challenges for Mobile, Wearable, Robotic, and IoT Platforms</h2>

    <div class="research-grid">
      <article class="research-topic-card" id="ai-optimization-project">
        <h3 class="research-topic-title">AI-Assisted Mobile System Optimization</h3>
        <div class="research-topic-copy">
          <p>We study how AI can help mobile and sensing systems make better decisions about communication, adaptation, and resource management under real-world constraints.</p>
          <ul>
            <li>Using foundation and generative models to improve system efficiency, communication, and deployment practicality.</li>
            <li>Designing adaptive mobile systems under limited bandwidth, compute, and storage budgets.</li>
          </ul>
        </div>
        <div class="research-topic-media">
          <img src="{{ "images/kdc.png" | relative_url }}" alt="KDC preview">
        </div>
        <div class="research-topic-links">
          <h4>Selected Publications</h4>
          <ul>
            <li><a href="{{ "/projects/" | relative_url }}?search=KDC">KDC</a> [<span class="research-pub-strong">NSDI'26</span>] <span class="research-paper-note">knowledge-driven communication of multimodal data using MLLM</span></li>
            <li><a href="{{ "/projects/" | relative_url }}?search=RFCanvas">RFCanvas</a> [<span class="research-pub-strong">SenSys'24</span>] <span class="research-paper-note">modeling RF channels using visual priors</span></li>
          </ul>
        </div>
      </article>

      <article class="research-topic-card" id="secure-sensing-project">
        <h3 class="research-topic-title">AI-Native Secure and Privacy-Preserving Sensing</h3>
        <div class="research-topic-copy">
          <p>We develop both attacks and defenses to better understand the trust, privacy, and security boundaries of sensing systems.</p>
          <ul>
            <li>Studying how sensing modalities can leak private information or be manipulated by adversaries.</li>
            <li>Designing practical defenses for mobile, acoustic, RF, and AI-driven sensing platforms.</li>
          </ul>
        </div>
        <div class="research-topic-media">
          <a href="https://www.youtube.com/watch?v=Vgy-u9HlQOo" target="_blank">
            <img src="{{ "images/magicpatch.gif" | relative_url }}" alt="MagicPatch preview">
          </a>
        </div>
        <div class="research-topic-links">
          <h4>Selected Publications</h4>
          <ul>
            <li><a href="https://www.youtube.com/watch?v=Vgy-u9HlQOo">MagicPatch</a> [<span class="research-pub-strong">MobiCom'26</span>] <span class="research-paper-note">mmWave imaging screening attack using metasurfaces</span></li>
            <li><a href="{{ "/projects/" | relative_url }}?search=EveGuard">EveGuard</a> [<span class="research-pub-strong">S&amp;P'25</span>] <span class="research-paper-note">perturbation defense against vibration eavesdropping</span></li>
            <li><a href="{{ "/projects/" | relative_url }}?search=Magmaw">Magmaw</a> [<span class="research-pub-strong">NDSS'25</span>] <span class="research-paper-note">adversarial attacks on ML-based wireless communication</span></li>
            <li><a href="{{ "/projects/" | relative_url }}?search=StealthyIMU">StealthyIMU</a> [<span class="research-pub-strong">NDSS'23</span>] <span class="research-paper-note">zero-permission sensor privacy attack using motion sensors</span></li>
          </ul>
        </div>
      </article>

      <article class="research-topic-card" id="native-ai-mobile-project">
        <h3 class="research-topic-title">Sensing-Assisted Native AI Mobile System</h3>
        <div class="research-topic-copy">
          <p>This direction explores mobile systems that use sensing to support more adaptive and context-aware native AI capabilities on personal devices.</p>
        </div>
        <div class="research-topic-media">
          <div class="research-topic-placeholder">In Submission</div>
        </div>
        <div class="research-topic-links">
          <h4>Related News</h4>
          <ul>
            <li><a href="https://cse.engin.umich.edu/stories/samsung-start-funds-cse-researchers-wearable-memory-augmentation-system" target="_blank">Samsung START funds CSE researchers' wearable memory augmentation system</a></li>
          </ul>
        </div>
      </article>

      <article class="research-topic-card" id="ai-mobile-sensing-project">
        <h3 class="research-topic-title">AI-Assisted Mobile Sensing System</h3>
        <div class="research-topic-copy">
          <p>This area studies how AI models and sensing pipelines can co-adapt to make mobile sensing systems more robust, data-efficient, and deployable.</p>
        </div>
        <div class="research-topic-media">
          <div class="research-topic-placeholder">Ongoing</div>
        </div>
        <div class="research-topic-links">
          <h4>Status</h4>
          <ul>
            <li>Ongoing project</li>
          </ul>
        </div>
      </article>

      <article class="research-topic-card" id="wearable-memory-project">
        <h3 class="research-topic-title">Wearable Agentic AI Memory System</h3>
        <div class="research-topic-copy">
          <p>This project studies wearable AI systems that can capture, organize, and retrieve important personal experiences to support human memory in everyday life.</p>
        </div>
        <div class="research-topic-media">
          <div class="research-topic-placeholder">Ongoing</div>
        </div>
        <div class="research-topic-links">
          <h4>Related News</h4>
          <ul>
            <li><a href="https://cse.engin.umich.edu/stories/samsung-start-funds-cse-researchers-wearable-memory-augmentation-system" target="_blank">Samsung START funds CSE researchers' wearable memory augmentation system</a></li>
          </ul>
        </div>
      </article>
    </div>
  </section>
</div>
