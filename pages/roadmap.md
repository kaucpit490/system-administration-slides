<style>
.roadmap-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
  padding: 10px;
  width: 100%;
  max-height: 90vh;
  margin-bottom: 40px;
}

.module-card {
  background: white;
  border-radius: 8px;
  padding: 15px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.module-card:hover {
  transform: translateY(-3px);
}

.module-number {
  display: inline-block;
  padding: 2px 6px;
  border-radius: 10px;
  color: white;
  font-size: 0.8em;
  margin-bottom: 4px;
}

.module-title {
  font-size: 1.3em;
  font-weight: bold;
  color: #2c3e50;
  margin-bottom: 4px;
}

.module-desc {
  font-size: 0.75em;
  color: #666;
  line-height: 1.2;
}

.m1 { background: #e74c3c; }
.m2 { background: #2ecc71; }
.m3 { background: #f1c40f; }
.m4 { background: #9b59b6; }
.m5 { background: #e67e22; }
.m6 { background: #3498db; }
</style>

<h3>Course Roadmap</h3>
<div class="roadmap-grid">
  <div class="module-card">
    <span class="module-number m1">Module 1</span>
    <div class="module-title">UNIX and Linux Fundamentals</div>
    <div class="module-desc">Core concepts of system administration, UNIX/Linux systems, file systems, and shell scripting fundamentals.</div>
  </div>

  <div class="module-card">
    <span class="module-number m2">Module 2</span>
    <div class="module-title">Cloud Computing and Deployment</div>
    <div class="module-desc">Cloud platforms, service fundamentals, and application deployment strategies.</div>
  </div>

  <div class="module-card">
    <span class="module-number m3">Module 3</span>
    <div class="module-title">Networking and Virtualization</div>
    <div class="module-desc">Network administration, virtualization technologies, and container management.</div>
  </div>

  <div class="module-card">
    <span class="module-number m4">Module 4</span>
    <div class="module-title">Performance Management</div>
    <div class="module-desc">System logging, performance monitoring, and analysis tools.</div>
  </div>

  <div class="module-card">
    <span class="module-number m5">Module 5</span>
    <div class="module-title">Software Management</div>
    <div class="module-desc">Configuration management, version control, and automation tools.</div>
  </div>

  <div class="module-card">
    <span class="module-number m6">Module 6</span>
    <div class="module-title">Machine Learning on the Cloud</div>
    <div class="module-desc">Cloud-based machine learning implementations and deployments.</div>
  </div>
</div>