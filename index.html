<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Payment Tracking System</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            background: white;
            border-radius: 15px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            overflow: hidden;
        }

        .header {
            background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
            color: white;
            padding: 30px;
            text-align: center;
            position: relative;
        }

        .header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
            text-shadow: 0 2px 4px rgba(0,0,0,0.3);
        }

        .firebase-status {
            position: absolute;
            top: 15px;
            right: 20px;
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 600;
            background: rgba(255,255,255,0.2);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.3);
        }

        .firebase-status.connected { background: rgba(40, 167, 69, 0.2); border-color: #28a745; }
        .firebase-status.disconnected { background: rgba(220, 53, 69, 0.2); border-color: #dc3545; }
        .firebase-status.connecting { background: rgba(255, 193, 7, 0.2); border-color: #ffc107; }

        .controls {
            padding: 30px;
            background: #f8f9fa;
            border-bottom: 1px solid #e9ecef;
        }

        .month-selector {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 20px;
            margin-bottom: 20px;
        }

        .month-nav-btn {
            background: #007bff;
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 16px;
            transition: all 0.3s;
        }

        .month-nav-btn:hover {
            background: #0056b3;
            transform: translateY(-2px);
        }

        .current-month {
            font-size: 24px;
            font-weight: bold;
            color: #333;
            text-align: center;
            min-width: 200px;
        }

        .add-entry-section {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
            align-items: end;
        }

        .form-group {
            display: flex;
            flex-direction: column;
        }

        .form-group label {
            margin-bottom: 5px;
            font-weight: 600;
            color: #333;
        }

        .form-group input, .form-group textarea {
            padding: 12px;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-size: 14px;
            transition: border-color 0.3s;
        }

        .form-group input:focus, .form-group textarea:focus {
            outline: none;
            border-color: #007bff;
        }

        .add-btn {
            background: linear-gradient(135deg, #28a745, #20c997);
            color: white;
            border: none;
            padding: 12px 24px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 16px;
            font-weight: 600;
            transition: all 0.3s;
            position: relative;
        }

        .add-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(40, 167, 69, 0.3);
        }

        .add-btn:disabled {
            opacity: 0.7;
            cursor: not-allowed;
            transform: none;
            box-shadow: none;
        }

        .loading {
            display: inline-block;
            width: 16px;
            height: 16px;
            border: 2px solid rgba(255,255,255,0.3);
            border-radius: 50%;
            border-top-color: white;
            animation: spin 0.8s ease-in-out infinite;
            margin-left: 8px;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }

        .summary-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            padding: 30px;
            background: #f8f9fa;
        }

        .summary-card {
            background: white;
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
            text-align: center;
            transition: transform 0.3s;
        }

        .summary-card:hover {
            transform: translateY(-5px);
        }

        .summary-card h3 {
            color: #666;
            margin-bottom: 10px;
            font-size: 14px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .summary-amount {
            font-size: 28px;
            font-weight: bold;
            color: #333;
        }

        .positive { color: #28a745; }
        .negative { color: #dc3545; }

        .table-container {
            padding: 30px;
            overflow-x: auto;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
        }

        th {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 15px 12px;
            text-align: center;
            font-weight: 600;
            font-size: 14px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        td {
            padding: 15px 12px;
            text-align: center;
            border-bottom: 1px solid #f1f3f4;
        }

        .date-cell { width: 120px; }
        .amount-cell { width: 120px; font-weight: 600; }
        .comments-cell { text-align: left; max-width: 200px; }
        .total-cell { background: #f8f9fa; font-weight: bold; }

        .delete-btn {
            background: #dc3545;
            color: white;
            border: none;
            padding: 6px 12px;
            border-radius: 6px;
            cursor: pointer;
            font-size: 12px;
            transition: all 0.3s;
        }

        .delete-btn:hover {
            background: #c82333;
            transform: scale(1.05);
        }

        .delete-btn:disabled {
            opacity: 0.5;
            cursor: not-allowed;
            transform: none;
        }

        .report-section {
            padding: 30px;
            background: #f8f9fa;
            border-top: 1px solid #e9ecef;
        }

        .report-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 25px;
        }

        .report-title {
            font-size: 24px;
            font-weight: bold;
            color: #333;
        }

        .generate-report-btn {
            background: linear-gradient(135deg, #6f42c1, #e83e8c);
            color: white;
            border: none;
            padding: 12px 24px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 16px;
            font-weight: 600;
            transition: all 0.3s;
        }

        .generate-report-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(111, 66, 193, 0.3);
        }

        .report-content {
            background: white;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
            display: none;
        }

        .report-content.show {
            display: block;
        }

        .report-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin-bottom: 30px;
        }

        .report-card {
            padding: 20px;
            border: 2px solid #e9ecef;
            border-radius: 10px;
            transition: all 0.3s;
        }

        .report-card:hover {
            border-color: #007bff;
            transform: translateY(-2px);
        }

        .report-card h4 {
            color: #333;
            margin-bottom: 15px;
            font-size: 18px;
            text-align: center;
        }

        .report-row {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
            padding: 8px 0;
            border-bottom: 1px solid #f1f3f4;
        }

        .report-row:last-child {
            border-bottom: none;
            font-weight: bold;
            margin-top: 10px;
            padding-top: 15px;
            border-top: 2px solid #e9ecef;
        }

        .toast {
            position: fixed;
            top: 20px;
            right: 20px;
            padding: 15px 20px;
            border-radius: 8px;
            color: white;
            font-weight: 600;
            z-index: 1000;
            transform: translateX(400px);
            transition: transform 0.3s;
        }

        .toast.show {
            transform: translateX(0);
        }

        .toast.success { background: #28a745; }
        .toast.error { background: #dc3545; }
        .toast.info { background: #17a2b8; }

        @media (max-width: 768px) {
            .add-entry-section {
                grid-template-columns: 1fr;
            }
            
            .summary-cards {
                grid-template-columns: 1fr;
            }
            
            .month-selector {
                flex-direction: column;
                gap: 15px;
            }
            
            table {
                font-size: 14px;
            }
            
            th, td {
                padding: 10px 8px;
            }

            .firebase-status {
                position: static;
                margin-top: 10px;
                display: inline-block;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <div class="firebase-status" id="firebaseStatus">Connecting...</div>
            <h1>💰 Payment Tracking System</h1>
            <p>Track Child Support, Health Insurance & Tutor Payments</p>
        </div>

        <div class="controls">
            <div class="month-selector">
                <button class="month-nav-btn" onclick="changeMonth(-1)">← Previous</button>
                <div class="current-month" id="currentMonth"></div>
                <button class="month-nav-btn" onclick="changeMonth(1)">Next →</button>
            </div>

            <div class="add-entry-section">
                <div class="form-group">
                    <label for="entryDate">Date:</label>
                    <input type="date" id="entryDate">
                </div>
                <div class="form-group">
                    <label for="childSupport">Child Support ($):</label>
                    <input type="number" id="childSupport" step="0.01" placeholder="0.00">
                </div>
                <div class="form-group">
                    <label for="healthInsurance">Health Insurance ($):</label>
                    <input type="number" id="healthInsurance" step="0.01" placeholder="0.00">
                </div>
                <div class="form-group">
                    <label for="tutor">Tutor ($):</label>
                    <input type="number" id="tutor" step="0.01" placeholder="0.00">
                </div>
                <div class="form-group">
                    <label for="extra">Extra ($):</label>
                    <input type="number" id="extra" step="0.01" placeholder="0.00">
                </div>
                <div class="form-group">
                    <label for="comments">Comments:</label>
                    <input type="text" id="comments" placeholder="Optional notes">
                </div>
                <div class="form-group">
                    <button class="add-btn" id="addBtn" onclick="addEntry()">Add Entry</button>
                </div>
            </div>
        </div>

        <div class="summary-cards">
            <div class="summary-card">
                <h3>Child Support</h3>
                <div class="summary-amount" id="childSupportTotal">$0.00</div>
                <div>Expected: $1,000.00</div>
                <div id="childSupportDiff" class="summary-amount">Difference: $0.00</div>
            </div>
            <div class="summary-card">
                <h3>Health Insurance</h3>
                <div class="summary-amount" id="healthInsuranceTotal">$0.00</div>
                <div>Expected: $363.00</div>
                <div id="healthInsuranceDiff" class="summary-amount">Difference: $0.00</div>
            </div>
            <div class="summary-card">
                <h3>Tutor Payments</h3>
                <div class="summary-amount" id="tutorTotal">$0.00</div>
                <div>Expected: $160.00</div>
                <div id="tutorDiff" class="summary-amount">Difference: $0.00</div>
            </div>
            <div class="summary-card">
                <h3>Monthly Total</h3>
                <div class="summary-amount" id="monthlyTotal">$0.00</div>
                <div>Expected: $1,523.00</div>
                <div id="monthlyDiff" class="summary-amount">Difference: $0.00</div>
            </div>
        </div>

        <div class="table-container">
            <table>
                <thead>
                    <tr>
                        <th class="date-cell">Date</th>
                        <th class="amount-cell">Child Support</th>
                        <th class="amount-cell">Health Insurance</th>
                        <th class="amount-cell">Tutor</th>
                        <th class="amount-cell">Extra</th>
                        <th class="comments-cell">Comments</th>
                        <th class="amount-cell">Weekly Total</th>
                        <th>Action</th>
                    </tr>
                </thead>
                <tbody id="entriesTable">
                    <!-- Entries will be added here -->
                </tbody>
            </table>
        </div>

        <div class="report-section">
            <div class="report-header">
                <h2 class="report-title">📊 Monthly Report</h2>
                <button class="generate-report-btn" onclick="toggleReport()">Generate Report</button>
            </div>
            <div class="report-content" id="reportContent">
                <div class="report-grid" id="reportGrid">
                    <!-- Report content will be generated here -->
                </div>
            </div>
        </div>
    </div>

    <!-- Firebase SDK -->
    <script type="module">
        // Import the functions you need from the SDKs you need
        import { initializeApp } from 'https://www.gstatic.com/firebasejs/10.0.0/firebase-app.js';
        import { getFirestore, collection, addDoc, getDocs, deleteDoc, doc, onSnapshot, query, orderBy } from 'https://www.gstatic.com/firebasejs/10.0.0/firebase-firestore.js';

        // TODO: Replace with your Firebase config
        const firebaseConfig = {
            apiKey: "AIzaSyD1_PzSHl4FImc7RI_6SbpSswYn3Mc1MzA",
            authDomain: "childsupport2jewel.firebaseapp.com",
            projectId: "childsupport2jewel",
            storageBucket: "childsupport2jewel.firebasestorage.app",
            messagingSenderId: "489454449895",
            appId: "1:489454449895:web:1741655f9a69dd65259e42"
        };

        // Initialize Firebase
        const app = initializeApp(firebaseConfig);
        const db = getFirestore(app);

        // Global variables
        window.db = db;
        window.collection = collection;
        window.addDoc = addDoc;
        window.getDocs = getDocs;
        window.deleteDoc = deleteDoc;
        window.doc = doc;
        window.onSnapshot = onSnapshot;
        window.query = query;
        window.orderBy = orderBy;

        // Initialize app after Firebase is loaded
        window.initializeApp();
    </script>

    <script>
        // Data storage
        let currentDate = new Date();
        let entries = {};
        let isLoading = false;
        let unsubscribe = null;
        
        // Expected amounts
        const expectedAmounts = {
            childSupport: 1000,
            healthInsurance: 363,
            tutor: 160
        };

        // Initialize
        window.initializeApp = function() {
            document.getElementById('entryDate').value = formatDateForInput(new Date());
            setupFirebaseListener();
            updateFirebaseStatus('connected');
            updateDisplay();
        };

        function formatDateForInput(date) {
            return date.toISOString().split('T')[0];
        }

        function formatDateForDisplay(date) {
            return date.toLocaleDateString('en-US', { 
                year: 'numeric', 
                month: 'long',
                day: 'numeric'
            });
        }

        function formatCurrency(amount) {
            return new Intl.NumberFormat('en-US', {
                style: 'currency',
                currency: 'USD'
            }).format(amount);
        }

        function getMonthKey(date) {
            return `${date.getFullYear()}-${date.getMonth()}`;
        }

        function updateFirebaseStatus(status) {
            const statusEl = document.getElementById('firebaseStatus');
            statusEl.className = `firebase-status ${status}`;
            
            switch(status) {
                case 'connected':
                    statusEl.textContent = '🟢 Connected to Firebase';
                    break;
                case 'disconnected':
                    statusEl.textContent = '🔴 Disconnected';
                    break;
                case 'connecting':
                    statusEl.textContent = '🟡 Connecting...';
                    break;
            }
        }

        function showToast(message, type = 'info') {
            // Remove existing toast
            const existingToast = document.querySelector('.toast');
            if (existingToast) {
                existingToast.remove();
            }

            const toast = document.createElement('div');
            toast.className = `toast ${type}`;
            toast.textContent = message;
            document.body.appendChild(toast);

            setTimeout(() => toast.classList.add('show'), 100);
            setTimeout(() => {
                toast.classList.remove('show');
                setTimeout(() => toast.remove(), 300);
            }, 3000);
        }

        function setupFirebaseListener() {
            try {
                const q = window.query(window.collection(window.db, 'payments'), window.orderBy('date', 'desc'));
                
                unsubscribe = window.onSnapshot(q, (snapshot) => {
                    entries = {};
                    
                    snapshot.docs.forEach(doc => {
                        const data = doc.data();
                        const entryDate = new Date(data.date);
                        const monthKey = getMonthKey(entryDate);
                        
                        if (!entries[monthKey]) {
                            entries[monthKey] = [];
                        }
                        
                        entries[monthKey].push({
                            id: doc.id,
                            ...data
                        });
                    });
                    
                    updateDisplay();
                }, (error) => {
                    console.error('Firebase listener error:', error);
                    updateFirebaseStatus('disconnected');
                    showToast('Connection to database lost', 'error');
                });
            } catch (error) {
                console.error('Setup listener error:', error);
                updateFirebaseStatus('disconnected');
                showToast('Failed to connect to database', 'error');
            }
        }

        function changeMonth(direction) {
            currentDate.setMonth(currentDate.getMonth() + direction);
            updateDisplay();
        }

        function updateDisplay() {
            // Update month display
            document.getElementById('currentMonth').textContent = 
                currentDate.toLocaleDateString('en-US', { year: 'numeric', month: 'long' });
            
            updateTable();
            updateSummary();
        }

        async function addEntry() {
            const date = document.getElementById('entryDate').value;
            const childSupport = parseFloat(document.getElementById('childSupport').value) || 0;
            const healthInsurance = parseFloat(document.getElementById('healthInsurance').value) || 0;
            const tutor = parseFloat(document.getElementById('tutor').value) || 0;
            const extra = parseFloat(document.getElementById('extra').value) || 0;
            const comments = document.getElementById('comments').value;

            if (!date) {
                showToast('Please select a date', 'error');
                return;
            }

            if (isLoading) return;
            
            isLoading = true;
            const addBtn = document.getElementById('addBtn');
            addBtn.disabled = true;
            addBtn.innerHTML = 'Adding... <div class="loading"></div>';

            try {
                const entry = {
                    date: date,
                    childSupport: childSupport,
                    healthInsurance: healthInsurance,
                    tutor: tutor,
                    extra: extra,
                    comments: comments,
                    total: childSupport + healthInsurance + tutor + extra,
                    timestamp: new Date().toISOString()
                };

                await window.addDoc(window.collection(window.db, 'payments'), entry);
                
                // Clear form
                document.getElementById('childSupport').value = '';
                document.getElementById('healthInsurance').value = '';
                document.getElementById('tutor').value = '';
                document.getElementById('extra').value = '';
                document.getElementById('comments').value = '';
                
                showToast('Entry added successfully!', 'success');
            } catch (error) {
                console.error('Error adding entry:', error);
                showToast('Failed to add entry. Please try again.', 'error');
            } finally {
                isLoading = false;
                addBtn.disabled = false;
                addBtn.innerHTML = 'Add Entry';
            }
        }

        async function deleteEntry(entryId) {
            if (!confirm('Are you sure you want to delete this entry?')) return;
            
            try {
                await window.deleteDoc(window.doc(window.db, 'payments', entryId));
                showToast('Entry deleted successfully!', 'success');
            } catch (error) {
                console.error('Error deleting entry:', error);
                showToast('Failed to delete entry. Please try again.', 'error');
            }
        }

        function updateTable() {
            const monthKey = getMonthKey(currentDate);
            const monthEntries = entries[monthKey] || [];
            const tbody = document.getElementById('entriesTable');
            
            tbody.innerHTML = '';
            
            // Sort entries by date (newest first)
            monthEntries.sort((a, b) => new Date(b.date) - new Date(a.date));
            
            monthEntries.forEach(entry => {
                const row = tbody.insertRow();
                row.innerHTML = `
                    <td class="date-cell">${formatDateForDisplay(new Date(entry.date))}</td>
                    <td class="amount-cell">${formatCurrency(entry.childSupport)}</td>
                    <td class="amount-cell">${formatCurrency(entry.healthInsurance)}</td>
                    <td class="amount-cell">${formatCurrency(entry.tutor)}</td>
                    <td class="amount-cell">${formatCurrency(entry.extra)}</td>
                    <td class="comments-cell">${entry.comments}</td>
                    <td class="amount-cell total-cell">${formatCurrency(entry.total)}</td>
                    <td><button class="delete-btn" onclick="deleteEntry('${entry.id}')">Delete</button></td>
                `;
            });

            if (monthEntries.length === 0) {
                const row = tbody.insertRow();
                row.innerHTML = `<td colspan="8" style="text-align: center; padding: 40px; color: #666;">No entries for this month</td>`;
            }
        }

        function updateSummary() {
            const monthKey = getMonthKey(currentDate);
            const monthEntries = entries[monthKey] || [];
            
            const totals = monthEntries.reduce((acc, entry) => {
                acc.childSupport += entry.childSupport;
                acc.healthInsurance += entry.healthInsurance;
                acc.tutor += entry.tutor;
                acc.extra += entry.extra;
                acc.total += entry.total;
                return acc;
            }, { childSupport: 0, healthInsurance: 0, tutor: 0, extra: 0, total: 0 });

            // Update summary cards
            document.getElementById('childSupportTotal').textContent = formatCurrency(totals.childSupport);
            document.getElementById('healthInsuranceTotal').textContent = formatCurrency(totals.healthInsurance);
            document.getElementById('tutorTotal').textContent = formatCurrency(totals.tutor);
            document.getElementById('monthlyTotal').textContent = formatCurrency(totals.total);

            // Calculate differences
            const childSupportDiff = totals.childSupport - expectedAmounts.childSupport;
            const healthInsuranceDiff = totals.healthInsurance - expectedAmounts.healthInsurance;
            const tutorDiff = totals.tutor - expectedAmounts.tutor;
            const totalDiff = totals.total - (expectedAmounts.childSupport + expectedAmounts.healthInsurance + expectedAmounts.tutor);

            // Update difference displays
            updateDifferenceDisplay('childSupportDiff', childSupportDiff);
            updateDifferenceDisplay('healthInsuranceDiff', healthInsuranceDiff);
            updateDifferenceDisplay('tutorDiff', tutorDiff);
            updateDifferenceDisplay('monthlyDiff', totalDiff);
        }

        function updateDifferenceDisplay(elementId, difference) {
            const element = document.getElementById(elementId);
            const absAmount = Math.abs(difference);
            
            if (difference > 0) {
                element.textContent = `Overpaid: ${formatCurrency(absAmount)}`;
                element.className = 'summary-amount positive';
            } else if (difference < 0) {
                element.textContent = `Underpaid: ${formatCurrency(absAmount)}`;
                element.className = 'summary-amount negative';
            } else {
                element.textContent = 'Exactly paid';
                element.className = 'summary-amount';
            }
        }

        function toggleReport() {
            const reportContent = document.getElementById('reportContent');
            if (reportContent.classList.contains('show')) {
                reportContent.classList.remove('show');
            } else {
                generateReport();
                reportContent.classList.add('show');
            }
        }

        function generateReport() {
            const monthKey = getMonthKey(currentDate);
            const monthEntries = entries[monthKey] || [];
            const reportGrid = document.getElementById('reportGrid');
            
            const totals = monthEntries.reduce((acc, entry) => {
                acc.childSupport += entry.childSupport;
                acc.healthInsurance += entry.healthInsurance;
                acc.tutor += entry.tutor;
                acc.extra += entry.extra;
                acc.total += entry.total;
                return acc;
            }, { childSupport: 0, healthInsurance: 0, tutor: 0, extra: 0, total: 0 });

            const monthName = currentDate.toLocaleDateString('en-US', { year: 'numeric', month: 'long' });

            reportGrid.innerHTML = `
                <div class="report-card">
                    <h4>💰 Child Support Report</h4>
                    <div class="report-row">
                        <span>Expected:</span>
                        <span>${formatCurrency(expectedAmounts.childSupport)}</span>
                    </div>
                    <div class="report-row">
                        <span>Received:</span>
                        <span>${formatCurrency(totals.childSupport)}</span>
                    </div>
                    <div class="report-row ${totals.childSupport - expectedAmounts.childSupport >= 0 ? 'positive' : 'negative'}">
                        <span>Status:</span>
                        <span>${getPaymentStatus(totals.childSupport - expectedAmounts.childSupport)}</span>
                    </div>
                </div>

                <div class="report-card">
                    <h4>🏥 Health Insurance Report</h4>
                    <div class="report-row">
                        <span>Expected:</span>
                        <span>${formatCurrency(expectedAmounts.healthInsurance)}</span>
                    </div>
                    <div class="report-row">
                        <span>Received:</span>
                        <span>${formatCurrency(totals.healthInsurance)}</span>
                    </div>
                    <div class="report-row ${totals.healthInsurance - expectedAmounts.healthInsurance >= 0 ? 'positive' : 'negative'}">
                        <span>Status:</span>
                        <span>${getPaymentStatus(totals.healthInsurance - expectedAmounts.healthInsurance)}</span>
                    </div>
                </div>

                <div class="report-card">
                    <h4>📚 Tutor Payment Report</h4>
                    <div class="report-row">
                        <span>Expected:</span>
                        <span>${formatCurrency(expectedAmounts.tutor)}</span>
                    </div>
                    <div class="report-row">
                        <span>Received:</span>
                        <span>${formatCurrency(totals.tutor)}</span>
                    </div>
                    <div class="report-row ${totals.tutor - expectedAmounts.tutor >= 0 ? 'positive' : 'negative'}">
                        <span>Status:</span>
                        <span>${getPaymentStatus(totals.tutor - expectedAmounts.tutor)}</span>
                    </div>
                </div>

                <div class="report-card">
                    <h4>📊 Monthly Summary</h4>
                    <div class="report-row">
                        <span>Total Expected:</span>
                        <span>${formatCurrency(expectedAmounts.childSupport + expectedAmounts.healthInsurance + expectedAmounts.tutor)}</span>
                    </div>
                    <div class="report-row">
                        <span>Total Received:</span>
                        <span>${formatCurrency(totals.total)}</span>
                    </div>
                    <div class="report-row">
                        <span>Extra Payments:</span>
                        <span>${formatCurrency(totals.extra)}</span>
                    </div>
                    <div class="report-row">
                        <span>Number of Entries:</span>
                        <span>${monthEntries.length}</span>
                    </div>
                    <div class="report-row ${totals.total - (expectedAmounts.childSupport + expectedAmounts.healthInsurance + expectedAmounts.tutor) >= 0 ? 'positive' : 'negative'}">
                        <span>Overall Status:</span>
                        <span>${getPaymentStatus(totals.total - (expectedAmounts.childSupport + expectedAmounts.healthInsurance + expectedAmounts.tutor))}</span>
                    </div>
                </div>
            `;
        }

        function getPaymentStatus(difference) {
            if (difference > 0) {
                return `Overpaid by ${formatCurrency(Math.abs(difference))}`;
            } else if (difference < 0) {
                return `Underpaid by ${formatCurrency(Math.abs(difference))}`;
            } else {
                return 'Paid in Full ✓';
            }
        }

        // Handle page unload
        window.addEventListener('beforeunload', () => {
            if (unsubscribe) {
                unsubscribe();
            }
        });
    </script>
</body>
</html>
