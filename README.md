

---

# Vaporizer Garden Manager

Welcome to the Vaporizer Garden Manager! This ASP.NET project provides CRUD functionality for managing vaporizers, gardens, herbs, and suppliers. It's designed to efficiently organize and track various elements of vaporizer gardening.

## Features

- **Vaporizers:** Manage different types of vaporizers, including their specifications and compatibility with herbs.
- **Gardens:** Track information about gardens, including the herbs grown in each garden.
- **Herbs:** Maintain a catalog of herbs, specifying which herbs are grown in which gardens and are compatible with which vaporizers.
- **Suppliers:** Manage information about suppliers, including the vaporizers they provide.

## Models

1. **Vaporizers:**
   - Attributes: ID, Name, Description, SupplierID, Compatibility
   - Relationships: Belongs to one Supplier
   - Description: Represents different types of vaporizers available in the system. Each vaporizer can have only one supplier but may be compatible with multiple herbs.

2. **Garden:**
   - Attributes: ID, Name, Location, HerbID
   - Relationships: Grows one Herb
   - Description: Represents individual gardens where herbs are grown. Each garden can grow only one type of herb.

3. **Herbs:**
   - Attributes: ID, Name, Description
   - Relationships: Grown in many Gardens, Compatible with many Vaporizers
   - Description: Catalog of herbs grown in the gardens. Each herb can be grown in multiple gardens and may be compatible with multiple vaporizers.

4. **Suppliers:**
   - Attributes: ID, Name, ContactInfo
   - Relationships: Provides many Vaporizers
   - Description: Represents suppliers providing vaporizers. Each supplier can provide multiple vaporizers.

## Setup

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/vaporizer-garden-manager.git
   ```

2. **Database Configuration:**
   - Configure your database connection string in `appsettings.json`.

3. **Run Migrations:**
   ```bash
   dotnet ef database update
   ```

4. **Run the Application:**
   ```bash
   dotnet run
   ```

5. **Access the Application:**
   Navigate to `https://localhost:5001` in your web browser.

## Contributing

Contributions are welcome! If you'd like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create your feature branch: `git checkout -b feature/your-feature-name`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin feature/your-feature-name`.
5. Submit a pull request.

## License

This project is licensed under the Humber License - see the [LICENSE](LICENSE) file for details.

