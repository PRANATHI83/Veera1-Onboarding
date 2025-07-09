<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>HR Staff Management Dashboard</title>
  <link rel="icon" href="data:,"/> <!-- Prevent favicon 404 -->
  <style>
    /* ... your full CSS here, unchanged ... */
    /* For brevity, reuse the full style block you already shared */
  </style>
</head>
<body>
  <div class="container">
    <header>
      <h1>HR Staff Management</h1>
      <p style="color: #fffcfc; text-align: center;">"Individuals play the game, but teams beat the odds."</p>
    </header>

    <div class="search-bar">
      <input type="text" id="searchInput" placeholder="Search employees by name, department, or employee ID...">
    </div>

    <main class="employee-grid" id="dataContainer">
      <!-- Employee cards will be added here dynamically -->
    </main>
  </div>

  <!-- ✅ Modal Injected Below -->
  <div id="modal" class="modal">
    <div class="modal-content">
      <div class="modal-header">
        <img id="modalProfilePic" class="profile-pic" src="" alt="Profile Picture" onerror="this.src='https://via.placeholder.com/50'; this.alt='No Profile Picture'">
        <div class="info-container">
          <h2 id="modalHeader">Employee Name</h2>
          <span id="modalEmpId" class="emp-id"></span>
        </div>
        <div class="close-modal" onclick="hideModal()">×</div>
      </div>
      <div class="modal-body" id="modalBody"></div>
    </div>
  </div>

  <!-- ✅ Full Updated JavaScript -->
  <script>
    function formatDate(dateString) {
      if (!dateString) return 'N/A';
      const date = new Date(dateString);
      return date.toLocaleDateString('en-US', { year: 'numeric', month: 'long', day: 'numeric' });
    }

    async function fetchActiveEmployees() {
      try {
        const response = await fetch('http://13.235.79.61:3056/api/employees/active');
        if (!response.ok) throw new Error(`HTTP ${response.status}: ${await response.text()}`);
        const data = await response.json();
        renderEmployeeCards(data.data);
      } catch (error) {
        console.error('Error fetching active employees:', error);
        document.getElementById('dataContainer').innerHTML =
          `<p style="color: red; text-align: center;">Error loading employees: ${error.message}</p>`;
      }
    }

    function renderEmployeeCards(employees) {
      const dataContainer = document.getElementById('dataContainer');
      dataContainer.innerHTML = '';
      employees.forEach(employee => {
        const card = document.createElement('div');
        card.className = 'employee-card';
        card.innerHTML = `
          <div class="card-header">
            <img class="profile-pic" src="http://13.235.79.61:3056/api/onboarding/${employee.id}/file/profilePic" alt="Profile Picture" onerror="this.src='https://via.placeholder.com/50'; this.alt='No Profile Picture'">
            <div class="info-container">
              <h2>${employee.full_name}</h2>
              <span class="emp-id">${employee.emp_id || 'N/A'}</span>
            </div>
          </div>
          <div class="card-body">
            <div class="info-group"><label>Department:</label><span>${employee.department || 'N/A'}</span></div>
            <div class="info-group"><label>Position:</label><span>${employee.job_role || 'N/A'}</span></div>
            <div class="info-group"><label>Join Date:</label><span>${formatDate(employee.job_start_date)}</span></div>
            <div class="info-group"><label>Status:</label><span>${employee.status || 'N/A'}</span></div>
          </div>
          <div class="card-footer">
            <button class="btn-view" onclick="showEmployeeDetails('${employee.id}')">View Details</button>
          </div>`;
        dataContainer.appendChild(card);
      });
    }

    async function showEmployeeDetails(employeeId) {
      try {
        const response = await fetch(`http://13.235.79.61:3056/api/onboarding/${employeeId}`);
        if (!response.ok) throw new Error(`HTTP ${response.status}: ${await response.text()}`);
        const employee = await response.json();

        document.getElementById('modalHeader').textContent = employee.full_name;
        document.getElementById('modalEmpId').textContent = employee.emp_id || 'N/A';
        document.getElementById('modalProfilePic').src = `http://13.235.79.61:3056/api/onboarding/${employee.id}/file/profilePic`;

        document.getElementById('modalBody').innerHTML = `
          <div class="details-section">
            <h3>Basic Information</h3>
            <div class="details-grid">
              <div class="detail-item"><label>Employee ID:</label><span>${employee.emp_id || 'N/A'}</span></div>
              <div class="detail-item"><label>Department:</label><span>${employee.department || 'N/A'}</span></div>
              <div class="detail-item"><label>Position:</label><span>${employee.job_role || 'N/A'}</span></div>
              <div class="detail-item"><label>Join Date:</label><span>${formatDate(employee.job_start_date)}</span></div>
              <div class="detail-item"><label>Status:</label><span>${employee.status || 'N/A'}</span></div>
            </div>
          </div>
          <div class="details-section">
            <h3>Contact Details</h3>
            <div class="details-grid">
              <div class="detail-item"><label>Email:</label><span>${employee.email || 'N/A'}</span></div>
              <div class="detail-item"><label>Date of Birth:</label><span>${formatDate(employee.dob)}</span></div>
              <div class="detail-item"><label>Phone:</label><span>${employee.phone || 'N/A'}</span></div>
              <div class="detail-item"><label>Address:</label><span>${employee.street_address || ''}, ${employee.city || ''}, ${employee.state || ''}, ${employee.zip_code || ''}</span></div>
              <div class="detail-item"><label>City:</label><span>${employee.city || 'N/A'}</span></div>
            </div>
          </div>
          <div class="details-section">
            <h3>Education Details</h3>
            <div class="details-grid">
              <div class="detail-item"><label>SSC Institution:</label><span>${employee.ssc_institution || 'N/A'}</span></div>
              <div class="detail-item"><label>SSC Year:</label><span>${employee.ssc_year || 'N/A'}</span></div>
              <div class="detail-item"><label>Intermediate Institution:</label><span>${employee.inter_institution || 'N/A'}</span></div>
              <div class="detail-item"><label>Intermediate Year:</label><span>${employee.inter_year || 'N/A'}</span></div>
              <div class="detail-item"><label>Highest Degree:</label><span>${employee.degree || 'N/A'}</span></div>
              <div class="detail-item"><label>Institution:</label><span>${employee.institution || 'N/A'}</span></div>
              <div class="detail-item"><label>Graduation Year:</label><span>${employee.graduation_year || 'N/A'}</span></div>
            </div>
          </div>
          <div class="details-section">
            <h3>Banking Details</h3>
            <div class="details-grid">
              <div class="detail-item"><label>Bank Name:</label><span>${employee.bank_name || 'N/A'}</span></div>
              <div class="detail-item"><label>Mobile Number:</label><span>${employee.mobile_number || 'N/A'}</span></div>
              <div class="detail-item"><label>Account Number:</label><span>${employee.account_number || 'N/A'}</span></div>
              <div class="detail-item"><label>IFSC Number:</label><span>${employee.ifsc_number || 'N/A'}</span></div>
            </div>
          </div>
          <div class="details-section">
            <h3>Emergency Contact</h3>
            <div class="details-grid">
              <div class="detail-item"><label>Name:</label><span>${employee.emergency_contact_name || 'N/A'}</span></div>
              <div class="detail-item"><label>Relationship:</label><span>${employee.emergency_contact_relationship || 'N/A'}</span></div>
              <div class="detail-item"><label>Phone:</label><span>${employee.emergency_contact_phone || 'N/A'}</span></div>
              <div class="detail-item"><label>Address:</label><span>${employee.emergency_contact_address || 'N/A'}</span></div>
            </div>
          </div>
        `;
        document.getElementById('modal').style.display = 'block';
      } catch (error) {
        console.error('Error fetching employee details:', error);
        alert(`Error loading employee details: ${error.message}`);
      }
    }

    function hideModal() {
      document.getElementById('modal').style.display = 'none';
    }

    document.addEventListener('DOMContentLoaded', () => {
      fetchActiveEmployees();

      document.getElementById('searchInput').addEventListener('input', async (e) => {
        const searchTerm = e.target.value.toLowerCase();
        try {
          const res = await fetch('http://13.235.79.61:3056/api/employees/active');
          if (!res.ok) throw new Error(`HTTP ${res.status}: ${await res.text()}`);
          const data = await res.json();
          const filtered = data.data.filter(emp => {
            const searchString = `${emp.full_name} ${emp.department || ''} ${emp.emp_id || ''}`.toLowerCase();
            return searchString.includes(searchTerm);
          });
          renderEmployeeCards(filtered);
        } catch (err) {
          console.error('Error searching employees:', err);
          document.getElementById('dataContainer').innerHTML =
            `<p style="color: red; text-align: center;">Error searching employees: ${err.message}</p>`;
        }
      });

      window.addEventListener('click', (event) => {
        if (event.target === document.getElementById('modal')) {
          hideModal();
        }
      });
    });
  </script>
</body>
</html>
