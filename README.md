# Templates

## Sparse Checkout

Sparse checkout allows you to check out only a specific directory from a repository.

### Steps

1. **Clone the repository with no checkout**:

   ```bash
   git clone --no-checkout https://github.com/ryikeda/templates.git
   cd templates
   ```

2. Enable sparse checkout:

   ```bash
   git sparse-checkout init --cone
   ```

3. Specify the path you want to check out:

   ```bash
   git sparse-checkout set docker-compose/portainer
   ```

4. Check out the files:

   ```bash
   git checkout
   ```

