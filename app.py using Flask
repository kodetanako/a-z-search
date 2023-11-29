from flask import Flask, render_template, request

app = Flask(__name__)

# Dummy data for search results
dummy_data = [
    "Result 1: Lorem ipsum dolor sit amet",
    "Result 2: Consectetur adipiscing elit",
    "Result 3: Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua",
    # Add more dummy data as needed
]

@app.route('/')
def index():
    return render_template('index.html')

@app.route('/search')
def search():
    query = request.args.get('query', '')
    results = [result for result in dummy_data if query.lower() in result.lower()]
    return render_template('index.html', results=results)

if __name__ == '__main__':
    app.run(debug=True)
