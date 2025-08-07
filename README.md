document.getElementById('login-form').addEventListener('submit', function(e) {
    e.preventDefault();
    const username = document.getElementById('username').value;
    const password = document.getElementById('password').value;
    const error = document.getElementById('error');

    // Dummy credentials
    if (username === 'admin' && password === '1234') {
        localStorage.setItem('isLoggedIn', 'true');
        window.location.href = 'create.html'; // Redirect to quiz creation
    } else {
        error.textContent = 'Invalid username or password';
    }
});