# urbanexplorer
Ce projet est une application web développée avec ReactJS permettant d’explorer différents lieux d’une ville : cafés, restaurants, hôtels, pharmacies, et autres services utiles
<!-- // ******************************************************************* -->
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Urban Explorer - Documentation Technique</title>
    <style>
        @page {
            margin: 2.5cm;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            color: #333;
            background: white;
            padding: 40px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .cover-page {
            text-align: center;
            padding: 100px 0;
            page-break-after: always;
        }

        .cover-title {
            font-size: 48px;
            color: #2E5090;
            font-weight: bold;
            margin-bottom: 20px;
        }

        .cover-subtitle {
            font-size: 24px;
            color: #666;
            margin-bottom: 10px;
        }

        .cover-description {
            font-size: 18px;
            font-style: italic;
            margin-bottom: 40px;
        }

        .project-info {
            max-width: 600px;
            margin: 40px auto;
            border: 2px solid #2E5090;
            border-radius: 8px;
        }

        .project-info table {
            width: 100%;
            border-collapse: collapse;
        }

        .project-info td {
            padding: 15px;
            border-bottom: 1px solid #ddd;
        }

        .project-info td:first-child {
            background: #E8F1F8;
            font-weight: bold;
            width: 40%;
        }

        h1 {
            color: #2E5090;
            font-size: 32px;
            margin: 40px 0 20px 0;
            padding-bottom: 10px;
            border-bottom: 3px solid #2E5090;
            page-break-before: always;
        }

        h2 {
            color: #2E5090;
            font-size: 24px;
            margin: 30px 0 15px 0;
        }

        h3 {
            color: #2E5090;
            font-size: 20px;
            margin: 20px 0 10px 0;
        }

        p {
            margin: 10px 0;
            text-align: justify;
        }

        ul, ol {
            margin: 10px 0 10px 30px;
        }

        li {
            margin: 5px 0;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }

        th, td {
            padding: 12px;
            border: 1px solid #ddd;
            text-align: left;
        }

        th {
            background: #2E5090;
            color: white;
            font-weight: bold;
        }

        tr:nth-child(even) {
            background: #f9f9f9;
        }

        .code-block {
            background: #f5f5f5;
            border-left: 4px solid #2E5090;
            padding: 15px;
            margin: 15px 0;
            font-family: 'Courier New', monospace;
            font-size: 14px;
            overflow-x: auto;
            white-space: pre;
        }

        .section-number {
            color: #2E5090;
            font-weight: bold;
        }

        .highlight {
            background: #fff3cd;
            padding: 2px 5px;
            border-radius: 3px;
        }

        .note {
            background: #e8f4fd;
            border-left: 4px solid #2196F3;
            padding: 15px;
            margin: 15px 0;
        }

        .phase-box {
            background: #f8f9fa;
            border: 2px solid #2E5090;
            border-radius: 8px;
            padding: 20px;
            margin: 20px 0;
        }

        .phase-title {
            color: #2E5090;
            font-size: 20px;
            font-weight: bold;
            margin-bottom: 10px;
        }

        @media print {
            body {
                padding: 0;
            }
            
            .page-break {
                page-break-after: always;
            }
            
            h1 {
                page-break-before: always;
            }
        }
    </style>
</head>
<body>

<!-- ==================== PAGE DE COUVERTURE ==================== -->
<div class="cover-page">
    <div class="cover-title">URBAN EXPLORER</div>
    <div class="cover-subtitle">Documentation Technique Complète</div>
    <div class="cover-description">Application Web Full-Stack de Découverte de Lieux</div>
    
    <div class="project-info">
        <table>
            <tr>
                <td>Technologies</td>
                <td>React + Vite, Redux Toolkit, Node.js + Express</td>
            </tr>
            <tr>
                <td>Base de Données</td>
                <td>MongoDB (localStorage en développement)</td>
            </tr>
            <tr>
                <td>Architecture</td>
                <td>MVC (Model-View-Controller) + Redux</td>
            </tr>
            <tr>
                <td>Fonctionnalités</td>
                <td>Auth, Filtres, Carte Interactive, Admin Panel</td>
            </tr>
        </table>
    </div>
</div>

<!-- ==================== TABLE DES MATIÈRES ==================== -->
<h1>Table des Matières</h1>
<ol>
    <li><a href="#intro">Introduction</a>
        <ul>
            <li>Présentation du Projet</li>
            <li>Objectifs</li>
            <li>Stack Technique</li>
        </ul>
    </li>
    <li><a href="#architecture">Architecture du Projet</a>
        <ul>
            <li>Structure des Dossiers</li>
            <li>Flow de Données</li>
            <li>Patterns Utilisés</li>
        </ul>
    </li>
    <li><a href="#features">Fonctionnalités Principales</a>
        <ul>
            <li>Système d'Authentification</li>
            <li>Gestion des Lieux</li>
            <li>Système de Filtrage</li>
            <li>Carte Interactive</li>
        </ul>
    </li>
    <li><a href="#development">Étapes de Développement</a>
        <ul>
            <li>Phase 0: Planification</li>
            <li>Phase 1: Setup</li>
            <li>Phase 2: Backend</li>
            <li>Phase 3: Frontend</li>
            <li>Phase 4: Intégration</li>
            <li>Phase 5: Déploiement</li>
        </ul>
    </li>
    <li><a href="#installation">Guide d'Installation</a></li>
    <li><a href="#conclusion">Conclusion</a></li>
</ol>

<!-- ==================== 1. INTRODUCTION ==================== -->
<h1 id="intro">1. Introduction</h1>

<h2>1.1 Présentation du Projet</h2>
<p>
    <strong>Urban Explorer</strong> est une application web full-stack permettant aux utilisateurs de découvrir, 
    explorer et interagir avec des lieux d'intérêt dans leur ville. L'application offre une expérience complète 
    avec authentification, filtrage avancé, carte interactive et gestion administrative.
</p>

<h2>1.2 Objectifs</h2>
<ul>
    <li>Permettre aux utilisateurs de découvrir des lieux (restaurants, parcs, cafés...)</li>
    <li>Offrir un système de filtrage puissant (catégorie, ville, note, distance)</li>
    <li>Fournir une carte interactive avec navigation GPS</li>
    <li>Gérer les utilisateurs avec différents rôles (User, Entreprise, Admin)</li>
    <li>Système de likes et favoris pour chaque lieu</li>
</ul>

<h2>1.3 Stack Technique</h2>
<table>
    <thead>
        <tr>
            <th>Composant</th>
            <th>Technologies</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>Frontend</strong></td>
            <td>React 18 + Vite, Redux Toolkit, React Router v6, Leaflet</td>
        </tr>
        <tr>
            <td><strong>Backend</strong></td>
            <td>Node.js, Express.js, MongoDB (ou localStorage)</td>
        </tr>
        <tr>
            <td><strong>State Management</strong></td>
            <td>Redux Toolkit (createSlice, createAsyncThunk)</td>
        </tr>
        <tr>
            <td><strong>Styling</strong></td>
            <td>CSS3, Responsive Design</td>
        </tr>
    </tbody>
</table>

<!-- ==================== 2. ARCHITECTURE ==================== -->
<h1 id="architecture">2. Architecture du Projet</h1>

<h2>2.1 Structure des Dossiers</h2>

<h3>Frontend Structure</h3>
<div class="code-block">frontend/
├── src/
│   ├── app/                  # Redux Store configuration
│   │   └── Store.jsx
│   ├── features/             # Fonctionnalités principales
│   │   ├── auth/            # Authentification
│   │   ├── places/          # Gestion des lieux
│   │   ├── filters/         # Filtres et recherche
│   │   ├── map/             # Carte interactive
│   │   └── admin/           # Panel administrateur
│   ├── pages/               # Pages de l'application
│   ├── components/          # Composants réutilisables
│   ├── services/            # Appels API
│   ├── utils/               # Fonctions utilitaires
│   ├── App.jsx              # Composant principal
│   └── main.jsx             # Point d'entrée
</div>

<h3>Backend Structure</h3>
<div class="code-block">backend/
├── src/
│   ├── models/              # Schémas de données
│   ├── routes/              # Routes API
│   ├── controllers/         # Logique métier
│   ├── middleware/          # Middleware (auth, validation)
│   ├── config/              # Configuration
│   └── server.js            # Point d'entrée
</div>

<h2>2.2 Flow de Données</h2>
<p>L'application utilise une architecture unidirectionnelle basée sur Redux :</p>
<ol>
    <li><strong>User Interaction</strong> - L'utilisateur interagit avec l'interface (click, input...)</li>
    <li><strong>Action Dispatch</strong> - Le composant déclenche une action via dispatch()</li>
    <li><strong>Redux Store Update</strong> - Le reducer met à jour le state global</li>
    <li><strong>Component Re-render</strong> - Les composants abonnés au state se mettent à jour</li>
    <li><strong>UI Update</strong> - L'interface utilisateur reflète les changements</li>
</ol>

<h2>2.3 Patterns Utilisés</h2>
<ul>
    <li><strong>MVC Pattern :</strong> Séparation Model-View-Controller</li>
    <li><strong>Redux Pattern :</strong> Single source of truth avec store centralisé</li>
    <li><strong>Component Pattern :</strong> Composants réutilisables et modulaires</li>
    <li><strong>HOC Pattern :</strong> Protected Routes pour la sécurité</li>
    <li><strong>Service Pattern :</strong> Encapsulation des appels API</li>
</ul>

<!-- ==================== 3. FONCTIONNALITÉS ==================== -->
<h1 id="features" style='color:red;'>3. Fonctionnalités Principales</h1>

<h2>3.1 Système d'Authentification</h2>

<h3>3.1.1 Inscription (Register)</h3>
<p><strong>Fonctionnalités :</strong></p>
<ul>
    <li>Validation des données (email, mot de passe, nom)</li>
    <li>Vérification d'unicité de l'email</li>
    <li>Hashage du mot de passe (bcrypt)</li>
    <li>Génération automatique de token JWT</li>
    <li>Stockage sécurisé dans localStorage</li>
    <li>Auto-login après inscription</li>
</ul>

<p><strong>Code Exemple (authSlice.js) :</strong></p>
<div class="code-block">export const register = createAsyncThunk(
  'auth/register',
  async (userData, { rejectWithValue }) => {
    try {
      const validation = validateRegister(userData);
      if (!validation.isValid) {
        return rejectWithValue(validation.errors);
      }
      
      const newUser = {
        id: Date.now().toString(),
        email: userData.email,
        password: hashPassword(userData.password),
        name: userData.name,
        role: userData.role || 'user',
        createdAt: new Date().toISOString()
      };
      
      storage.addUser(newUser);
      storage.login(newUser);
      
      return newUser;
    } catch (error) {
      return rejectWithValue({ general: error.message });
    }
  }
);
</div>

<h3>3.1.2 Connexion (Login)</h3>
<p><strong>Processus :</strong></p>
<ol>
    <li>Validation des credentials (email + password)</li>
    <li>Recherche de l'utilisateur dans la base</li>
    <li>Vérification du mot de passe</li>
    <li>Génération du token JWT</li>
    <li>Stockage du token et user dans localStorage</li>
    <li>Redirection vers le dashboard approprié</li>
</ol>

<h3>3.1.3 Gestion des Rôles</h3>
<table>
    <thead>
        <tr>
            <th>Rôle</th>
            <th>Permissions</th>
            <th>Routes Accessibles</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>User</strong></td>
            <td>Voir lieux, likes, favoris</td>
            <td>/user, /explore, /map</td>
        </tr>
        <tr>
            <td><strong>Entreprise</strong></td>
            <td>Ajouter/modifier ses lieux</td>
            <td>/entreprise, /entreprise/places</td>
        </tr>
        <tr>
            <td><strong>Admin</strong></td>
            <td>Gestion totale (users, places)</td>
            <td>/admin/*</td>
        </tr>
    </tbody>
</table>

<h2>3.2 Gestion des Lieux (Places)</h2>

<h3>3.2.1 Structure des Données</h3>
<div class="code-block">{
  id: "place_123",
  name: "Restaurant Saveur",
  description: "Restaurant traditionnel marocain",
  category: "restaurant",
  city: "Tangier",
  address: "Avenue Mohammed V",
  location: {
    lat: 35.7595,
    lng: -5.8339
  },
  rating: 4.5,
  image: "https://...",
  phone: "+212 xxx xxx xxx",
  openingHours: "09:00 - 23:00",
  likes: 150,
  favorites: 45,
  likedBy: ["user_1", "user_2"],
  favoritedBy: ["user_3"],
  createdBy: "entreprise_5",
  createdAt: "2024-01-15T10:30:00Z"
}
</div>

<h3>3.2.2 Opérations CRUD</h3>
<ul>
    <li><strong>Create (Ajouter un lieu) :</strong> Réservé aux entreprises et admins, validation des champs, géolocalisation</li>
    <li><strong>Read (Consulter) :</strong> Liste de tous les lieux publics, détails d'un lieu, filtrage avancé</li>
    <li><strong>Update (Modifier) :</strong> Propriétaire ou admin uniquement</li>
    <li><strong>Delete (Supprimer) :</strong> Admin uniquement</li>
</ul>

<h2>3.3 Système de Filtrage</h2>

<h3>3.3.1 Filtres Disponibles</h3>
<table>
    <thead>
        <tr>
            <th>Filtre</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Search</td>
            <td>Texte libre</td>
            <td>Recherche par nom</td>
        </tr>
        <tr>
            <td>Category</td>
            <td>Select dropdown</td>
            <td>Restaurant, Café, Parc...</td>
        </tr>
        <tr>
            <td>Rating</td>
            <td>Range 0-5</td>
            <td>Note minimale</td>
        </tr>
        <tr>
            <td>Distance</td>
            <td>Range 0-100 km</td>
            <td>Distance max depuis position</td>
        </tr>
    </tbody>
</table>

<h2>3.4 Carte Interactive</h2>

<h3>3.4.1 Technologies Utilisées</h3>
<ul>
    <li><strong>Leaflet.js :</strong> Bibliothèque de cartographie open-source</li>
    <li><strong>React-Leaflet :</strong> Wrapper React pour Leaflet</li>
    <li><strong>OpenStreetMap :</strong> Tuiles de carte gratuites</li>
</ul>

<h3>3.4.2 Fonctionnalités</h3>
<ul>
    <li>Affichage des lieux avec marqueurs personnalisés</li>
    <li>Géolocalisation de l'utilisateur</li>
    <li>Calcul d'itinéraire entre deux points</li>
    <li>Popup avec informations du lieu</li>
    <li>Zoom et navigation fluides</li>
    <li>Clustering pour performance</li>
</ul>

<!-- ==================== 4. ÉTAPES DE DÉVELOPPEMENT ==================== -->
<h1 id="development">4. Étapes de Développement</h1>

<div class="phase-box">
    <div class="phase-title">📋 Phase 0 : Planification (1-2 jours)</div>
    <ol>
        <li><strong>Définition du projet</strong> - Objectifs, fonctionnalités, rôles</li>
        <li><strong>Choix des technologies</strong> - React, Redux, Node.js, MongoDB</li>
        <li><strong>Design de la base de données</strong> - Schémas Users, Places</li>
        <li><strong>Maquettes UI/UX</strong> - Wireframes des pages</li>
    </ol>
</div>

<div class="phase-box">
    <div class="phase-title">🏗️ Phase 1 : Setup (1-2 heures)</div>
    <h4>Frontend Setup:</h4>
    <div class="code-block"># Créer projet Vite + React
npm create vite@latest frontend -- --template react

# Installer dépendances
npm install react-router-dom
npm install @reduxjs/toolkit react-redux
npm install leaflet react-leaflet

# Créer structure
mkdir -p src/features src/pages src/components
</div>

    <h4>Backend Setup:</h4>
    <div class="code-block"># Créer dossier backend
mkdir backend && cd backend

# Initialiser Node.js
npm init -y

# Installer dépendances
npm install express mongoose dotenv bcryptjs jsonwebtoken cors
npm install -D nodemon
</div>
</div>

<div class="phase-box">
    <div class="phase-title">🔧 Phase 2 : Backend (3-5 jours)</div>
    <ul>
        <li><strong>Jour 1 :</strong> Configuration serveur Express</li>
        <li><strong>Jour 2 :</strong> Connexion MongoDB + Modèles</li>
        <li><strong>Jours 3-4 :</strong> APIs & Controllers (auth, places)</li>
        <li><strong>Jour 5 :</strong> Tests avec Postman</li>
    </ul>
</div>

<div class="phase-box">
    <div class="phase-title">🎨 Phase 3 : Frontend (5-7 jours)</div>
    <ul>
        <li><strong>Jours 6-7 :</strong> Structure Redux + Router</li>
        <li><strong>Jours 8-9 :</strong> Pages Auth (Login/Register)</li>
        <li><strong>Jours 10-11 :</strong> Places & Filtres</li>
        <li><strong>Jours 12-13 :</strong> Carte Interactive + Admin</li>
    </ul>
</div>

<div class="phase-box">
    <div class="phase-title">🔗 Phase 4 : Intégration (1-2 jours)</div>
    <ul>
        <li>Connecter frontend et backend</li>
        <li>Tester le flux complet</li>
        <li>Gestion des erreurs</li>
        <li>Loading states</li>
    </ul>
</div>

<div class="phase-box">
    <div class="phase-title">✨ Phase 5 : Polish & Déploiement (2-3 jours)</div>
    <ul>
        <li>Amélioration design CSS</li>
        <li>Responsive design</li>
        <li>Optimisation performances</li>
        <li>Déploiement (Vercel + Render)</li>
    </ul>
</div>

<!-- ==================== 5. GUIDE D'INSTALLATION ==================== -->
<h1 id="installation">5. Guide d'Installation</h1>

<h2>5.1 Prérequis</h2>
<ul>
    <li>Node.js v18 ou supérieur</li>
    <li>npm ou yarn</li>
    <li>MongoDB (local ou Atlas)</li>
    <li>Git</li>
</ul>

<h2>5.2 Installation Backend</h2>
<div class="code-block"># 1. Cloner le repository
git clone https://github.com/username/urbanexplorer.git
cd urbanexplorer/backend

# 2. Installer les dépendances
npm install

# 3. Créer fichier .env
PORT=5000
MONGO_URI=mongodb://localhost:27017/urbanexplorer
JWT_SECRET=your_secret_key_here

# 4. Lancer le serveur
npm run dev
</div>

<h2>5.3 Installation Frontend</h2>
<div class="code-block"># 1. Naviguer vers frontend
cd ../frontend

# 2. Installer les dépendances
npm install

# 3. Lancer l'application
npm run dev
</div>

<h2>5.4 Variables d'Environnement</h2>
<table>
    <thead>
        <tr>
            <th>Variable</th>
            <th>Description</th>
            <th>Exemple</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>PORT</td>
            <td>Port du serveur</td>
            <td>5000</td>
        </tr>
        <tr>
            <td>MONGO_URI</td>
            <td>URI MongoDB</td>
            <td>mongodb://localhost:27017/db</td>
        </tr>
        <tr>
            <td>JWT_SECRET</td>
            <td>Clé secrète JWT</td>
            <td>your_secret_key</td>
        </tr>
    </tbody>
</table>

<!-- ==================== 6. CONCLUSION ==================== -->
<h1 id="conclusion">6. Conclusion</h1>

<h2>6.1 Résumé du Projet</h2>
<p>
    Urban Explorer est une application web complète qui démontre la maîtrise des technologies modernes 
    de développement full-stack. Le projet intègre avec succès React, Redux, Node.js, et MongoDB pour 
    créer une expérience utilisateur fluide et interactive.
</p>

<h2>6.2 Compétences Acquises</h2>
<ul>
    <li>Développement frontend avec React et Redux Toolkit</li>
    <li>Développement backend avec Node.js et Express</li>
    <li>Gestion de base de données MongoDB</li>
    <li>Authentification JWT et gestion des rôles</li>
    <li>Intégration de cartes interactives avec Leaflet</li>
    <li>Architecture MVC et patterns modernes</li>
    <li>Déploiement d'applications web</li>
</ul>

<h2>6.3 Améliorations Futures</h2>
<ul>
    <li>Système de reviews et commentaires</li>
    <li>Upload d'images pour les lieux</li>
    <li>Notifications en temps réel</li>
    <li>Application mobile React Native</li>
    <li>Intégration de paiement en ligne</li>
    <li>Analytics et statistiques avancées</li>
</ul>

<div style="text-align: center; margin-top: 60px; padding: 20px; font-style: italic; color: #666;">
    ― Fin du Document ―
</div>

</body>
</html>

<!-- <Route element={<ProtectedRoute />}>  // ← Khass tkoun logged in
  <Route element={<AdminRoute />}>     // ← Khass tkoun Admin
    <Route path="/admin" />
  </Route>
</Route>
```

**Kifash kaykhedem:**
1. User ybgha ydkhol l `/admin`
2. **ProtectedRoute** kay-check: wach logged in? ❌ → Redirect l `/login`
3. **AdminRoute** kay-check: wach role = admin? ❌ → Redirect l `/`
4. ✅ Ila kamlin → Ydkhol l Admin Dashboard

---

## **4️⃣ COMPLETE FLOW - Example Réel**

### **Scenario: User bghaa ychof Restaurants f Tangier**
```
┌─────────────────────────────────────────────────────────┐
│ STEP 1: User ydkhol l http://localhost:5173             │
└───────────┬─────────────────────────────────────────────┘
            ↓
┌─────────────────────────────────────────────────────────┐
│ STEP 2: main.jsx kay-setup                              │
│   - Redux Store t-créa                                  │
│   - BrowserRouter t-setup                               │
│   - App component t-render                              │
└───────────┬─────────────────────────────────────────────┘
            ↓
┌─────────────────────────────────────────────────────────┐
│ STEP 3: App.jsx kay-check URL                           │
│   URL = "/" → Route match ✅                            │
│   → Render <Home />                                     │
└───────────┬─────────────────────────────────────────────┘
            ↓
┌─────────────────────────────────────────────────────────┐
│ STEP 4: Home Page t-render                              │
│   - Hero section m3a search bar                         │
│   - Filters (Category, City, Rating...)                 │
└───────────┬─────────────────────────────────────────────┘
            ↓
┌─────────────────────────────────────────────────────────┐
│ STEP 5: User y-cliquer "Explore"                        │
│   → navigate('/explore')                                │
└───────────┬─────────────────────────────────────────────┘
            ↓
┌─────────────────────────────────────────────────────────┐
│ STEP 6: App.jsx kay-detect URL change                   │
│   URL = "/explore" → Route match ✅                     │
│   → Render <ExplorePage />                              │
└───────────┬─────────────────────────────────────────────┘
            ↓
┌─────────────────────────────────────────────────────────┐
│ STEP 7: ExplorePage component                           │
│   - Jib places men Redux Store                          │
│   - Afficher filters panel                              │
│   - Afficher places list                                │
└───────────┬─────────────────────────────────────────────┘
            ↓
┌─────────────────────────────────────────────────────────┐
│ STEP 8: User y-sélectionner filters                     │
│   - Category: "Restaurants"                             │
│   - City: "Tangier"                                     │
│   - Rating: 4+                                          │
│   → dispatch(setFilters({...}))                         │
└───────────┬─────────────────────────────────────────────┘
            ↓
┌─────────────────────────────────────────────────────────┐
│ STEP 9: Redux Store t-update                            │
│   state.filters = {                                     │
│     category: "Restaurants",                            │
│     city: "Tangier",                                    │
│     rating: 4                                           │
│   }                                                     │
└───────────┬─────────────────────────────────────────────┘
            ↓
┌─────────────────────────────────────────────────────────┐
│ STEP 10: Components y-re-render                         │
│   - PlacesList component tala7 update f Store           │
│   - Kay-filter places based on new filters              │
│   - Kay-afficher results (5 restaurants f Tangier)      │
└─────────────────────────────────────────────────────────┘
```

---

## **📊 Data Flow Diagram:**
```
User Action (Click/Type)
         ↓
Component dispatches action
         ↓
Redux Store updates state
         ↓
useSelector detects change
         ↓
Component re-renders with new data
         ↓
UI updates
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
main.jsx   - Setup l-application  - بناء الأساس
Store.jsx  - Stockage dyal data   - خزانة المعلومات 
App.jsx    - Navigation/Routing   - خريطة الطرق
Components - UI elements          - الواجهة 
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
<h1>PARTIE 1</h1> ***************************************************************************************************************************************************************************** -->
