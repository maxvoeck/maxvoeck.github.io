<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mathematik - Studienkolleg</title>
    <style>
        .materials-grid {
          display: grid;
          grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
          gap: 1.5rem;
          margin: 2rem 0;
        }

        .material-card {
          border: 1px solid #e0e0e0;
          border-radius: 8px;
          padding: 1.5rem;
          transition: box-shadow 0.3s ease;
          background: #fff;
        }

        .material-card:hover {
          box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .material-card h4 {
          margin-top: 0;
          color: #333;
          font-size: 1.1rem;
        }

        .material-card p {
          font-size: 0.9rem;
          color: #666;
          margin: 0.5rem 0 1rem 0;
        }

        .btn-small {
          display: inline-block;
          padding: 0.4rem 0.8rem;
          background: linear-gradient(135deg, #374151 0%, #1f2937 100%);
          color: white !important;
          text-decoration: none;
          border-radius: 4px;
          font-size: 0.85rem;
          transition: all 0.3s ease;
          margin-right: 0.5rem;
          margin-bottom: 0.5rem;
        }

        .btn-small:hover {
          background: linear-gradient(135deg, #4b5563 0%, #374151 100%);
          transform: translateY(-1px);
        }

        .btn-download {
          background: linear-gradient(135deg, #059669 0%, #047857 100%);
        }

        .btn-download:hover {
          background: linear-gradient(135deg, #10b981 0%, #059669 100%);
        }

        .btn-preview {
          background: linear-gradient(135deg, #2563eb 0%, #1d4ed8 100%);
        }

        .btn-preview:hover {
          background: linear-gradient(135deg, #3b82f6 0%, #2563eb 100%);
        }

        .section-header {
          border-bottom: 2px solid #374151;
          padding-bottom: 0.5rem;
          margin: 2rem 0 1rem 0;
          color: #1f2937;
        }

        .coming-soon {
          background: #f8f9fa;
          padding: 1rem;
          border-radius: 4px;
          color: #666;
          font-style: italic;
          border-left: 4px solid #374151;
        }

        .page-header {
          background: linear-gradient(135deg, #374151 0%, #1f2937 100%);
          color: white;
          padding: 2rem;
          margin: -2rem -2rem 2rem -2rem;
          border-radius: 0 0 12px 12px;
        }

        .page-header h1 {
          margin: 0;
          font-size: 2rem;
        }

        .back-link {
          display: inline-block;
          margin-top: 2rem;
          color: #374151;
          text-decoration: none;
          font-weight: 500;
          transition: color 0.3s ease;
        }

        .back-link:hover {
          color: #1f2937;
        }

        /* Suchfunktion Styling */
        .search-container {
          margin: 2rem 0;
          display: flex;
          gap: 1rem;
          flex-wrap: wrap;
        }

        #materialSearch {
          flex: 1;
          min-width: 250px;
          padding: 0.75rem 1rem;
          border: 1px solid #d1d5db;
          border-radius: 6px;
          font-size: 1rem;
          transition: border-color 0.3s ease;
        }

        #materialSearch:focus {
          outline: none;
          border-color: #374151;
          box-shadow: 0 0 0 3px rgba(55, 65, 81, 0.1);
        }

        #categoryFilter {
          padding: 0.75rem 1rem;
          border: 1px solid #d1d5db;
          border-radius: 6px;
          font-size: 1rem;
          background: white;
          cursor: pointer;
        }

        .no-results {
          text-align: center;
          padding: 2rem;
          color: #6b7280;
          font-style: italic;
          grid-column: 1 / -1;
        }

        /* Farbliche Kategorisierung */
        .vector-geometry { border-left: 4px solid #3b82f6; }
        .linear-algebra { border-left: 4px solid #10b981; }
        .differential { border-left: 4px solid #f59e0b; }
        .integral { border-left: 4px solid #ef4444; }

        /* Responsive Verbesserungen */
        @media (max-width: 768px) {
          .materials-grid {
            grid-template-columns: 1fr;
          }
          
          .page-header {
            margin: -1rem -1rem 2rem -1rem;
            padding: 1.5rem;
          }
          
          .page-header h1 {
            font-size: 1.5rem;
          }
          
          .search-container {
            flex-direction: column;
          }
          
          #materialSearch, #categoryFilter {
            width: 100%;
          }
        }

        @media (max-width: 480px) {
          .material-card {
            padding: 1rem;
            margin: 0.5rem 0;
          }
          
          .btn-small {
            display: block;
            text-align: center;
            margin: 0.5rem 0;
          }
          
          .page-header {
            padding: 1rem;
            margin: -1rem -1rem 1.5rem -1rem;
          }
        }
    </style>
</head>
<body>
    <div class="page-header">
        <h1>Mathematik</h1>
        <p>Materialien zur Prüfungsvorbereitung am Studienkolleg</p>
    </div>

    <!-- Such- und Filterfunktion -->
    <div class="search-container">
        <input type="text" id="materialSearch" placeholder="Materialien durchsuchen...">
        <select id="categoryFilter">
            <option value="all">Alle Kategorien</option>
            <option value="vektorrechnung">Vektorrechnung</option>
            <option value="lineare-algebra">Lineare Algebra</option>
            <option value="differentialrechnung">Differentialrechnung</option>
            <option value="integralrechnung">Integralrechnung</option>
        </select>
    </div>

    <h2 class="section-header">Vektorrechnung und Analytische Geometrie</h2>
    <div class="materials-grid">
        <div class="material-card vector-geometry" data-category="vektorrechnung">
            <h4>📐 Vektorrechnung – Grundlagen</h4>
            <p>Einführung in Vektoren, Koordinatensysteme, Skalare vs. vektorielle Größen, Betrag, Einheitsvektoren, Basisvektoren und Grundoperationen</p>
            <a href="/assets/pdfs/Geo_2_1-2.pdf" class="btn-small btn-preview" target="_blank">Vorschau</a>
            <a href="/assets/pdfs/Geo_2_1-2.pdf" class="btn-small btn-download" download>PDF herunterladen</a>
        </div>
        
        <div class="material-card vector-geometry" data-category="vektorrechnung">
            <h4>📏 Vektorprodukt und Spatprodukt</h4>
            <p>Kreuzprodukt, geometrische Bedeutung, Flächenberechnung, Spatprodukt, Volumenberechnung und Anwendungen in der Raumgeometrie</p>
            <a href="/assets/pdfs/Geo_2_2-2.pdf" class="btn-small btn-preview" target="_blank">Vorschau</a>
            <a href="/assets/pdfs/Geo_2_2-2.pdf" class="btn-small btn-download" download>PDF herunterladen</a>
        </div>
        
        <div class="material-card vector-geometry" data-category="vektorrechnung">
            <h4>📊 Geraden und Ebenen im Raum</h4>
            <p>Parametergleichungen von Geraden und Ebenen, Normalenvektor, Koordinatenform, Lagebeziehungen und Schnittwinkelberechnung</p>
            <a href="/assets/pdfs/Geo_2_3.pdf" class="btn-small btn-preview" target="_blank">Vorschau</a>
            <a href="/assets/pdfs/Geo_2_3.pdf" class="btn-small btn-download" download>PDF herunterladen</a>
        </div>
        
        <div class="material-card vector-geometry" data-category="vektorrechnung">
            <h4>📐 Lagebeziehungen und Abstände</h4>
            <p>Ebene-Ebene-Lagen, Abstandsberechnungen zwischen Punkten, Geraden und Ebenen, Hessesche Normalenform und praktische Anwendungen</p>
            <a href="/assets/pdfs/Geo_2_4.pdf" class="btn-small btn-preview" target="_blank">Vorschau</a>
            <a href="/assets/pdfs/Geo_2_4.pdf" class="btn-small btn-download" download>PDF herunterladen</a>
        </div>
    </div>

    <h2 class="section-header">Lineare Algebra</h2>
    <div class="materials-grid">
        <div class="material-card linear-algebra" data-category="lineare-algebra">
            <h4>📙 Matrizen – Einführung und Rechenoperationen</h4>
            <p>Grundlagen der Matrizenrechnung: Addition, Multiplikation, Transponieren, spezielle Matrizen und Rechenregeln mit praktischen Beispielen</p>
            <a href="/assets/pdfs/Matrizen_2_1-5.pdf" class="btn-small btn-preview" target="_blank">Vorschau</a>
            <a href="/assets/pdfs/Matrizen_2_1-5.pdf" class="btn-small btn-download" download>PDF herunterladen</a>
        </div>
        
        <div class="material-card linear-algebra" data-category="lineare-algebra">
            <h4>📕 Determinanten – Grundlagen und Rechenregeln</h4>
            <p>Determinantenberechnung, Laplace-Entwicklung, Sarrus-Regel, reguläre/singuläre Matrizen, geometrische Bedeutung und Inverse Matrizen</p>
            <a href="/assets/pdfs/Matrizen_2_2-2.pdf" class="btn-small btn-preview" target="_blank">Vorschau</a>
            <a href="/assets/pdfs/Matrizen_2_2-2.pdf" class="btn-small btn-download" download>PDF herunterladen</a>
        </div>
        
        <div class="material-card linear-algebra" data-category="lineare-algebra">
            <h4>📒 Matrizengleichungen – Übungsaufgaben</h4>
            <p>Umfangreiche Übungsaufgaben zu Matrizengleichungen, Rangbestimmung, Gauß-Elimination und Lösungsstrategien für verschiedene Matrixgrößen</p>
            <a href="/assets/pdfs/Matrizen_2_3-3.pdf" class="btn-small btn-preview" target="_blank">Vorschau</a>
            <a href="/assets/pdfs/Matrizen_2_3-3.pdf" class="btn-small btn-download" download>PDF herunterladen</a>
        </div>
        
        <div class="material-card linear-algebra" data-category="lineare-algebra">
            <h4>📘 Lineare Gleichungssysteme – Grundlagen</h4>
            <p>Einführung in LGS, Matrixschreibweise, Gauß-Algorithmus, Lösbarkeitskriterien und praktische Anwendungen in Ingenieurwesen und Wirtschaft</p>
            <a href="/assets/pdfs/LGS_2_1-5.pdf" class="btn-small btn-preview" target="_blank">Vorschau</a>
            <a href="/assets/pdfs/LGS_2_1-5.pdf" class="btn-small btn-download" download>PDF herunterladen</a>
        </div>
        
        <div class="material-card linear-algebra" data-category="lineare-algebra">
            <h4>📗 Lineare Gleichungssysteme – Parameterabhängigkeit</h4>
            <p>Untersuchung von LGS mit Parametern, Determinantentest, Fallunterscheidungen und Lösbarkeitsanalyse für verschiedene Parameterwerte</p>
            <a href="/assets/pdfs/LGS_2_2-2.pdf" class="btn-small btn-preview" target="_blank">Vorschau</a>
            <a href="/assets/pdfs/LGS_2_2-2.pdf" class="btn-small btn-download" download>PDF herunterladen</a>
        </div>
    </div>

    <h2 class="section-header">Differentialrechnung</h2>
    <div class="materials-grid">
        <div class="material-card differential" data-category="differentialrechnung">
            <h4>📘 Extremwertaufgaben</h4>
            <p>Systematisches Lösen von Optimierungsproblemen: Haupt- und Nebenbedingungen, Zielfunktionen, Kurvendiskussion mit Beispielen aus Technik und Wirtschaft</p>
            <a href="/assets/pdfs/Extrem_2_1.pdf" class="btn-small btn-preview" target="_blank">Vorschau</a>
            <a href="/assets/pdfs/Extrem_2_1.pdf" class="btn-small btn-download" download>PDF herunterladen</a>
        </div>
    </div>

    <h2 class="section-header">Integralrechnung</h2>
    <div class="materials-grid">
        <div class="material-card integral" data-category="integralrechnung">
            <h4>📘 Einführung</h4>
            <p>Stammfunktionen, Grundintegrale, Faktor- und Summenregel, bestimmtes Integral</p>
            <a href="/assets/pdfs/Integral_2_1.pdf" class="btn-small btn-preview" target="_blank">Vorschau</a>
            <a href="/assets/pdfs/Integral_2_1.pdf" class="btn-small btn-download" download>PDF herunterladen</a>
        </div>
        
        <div class="material-card integral" data-category="integralrechnung">
            <h4>📗 Integrationsmethoden</h4>
            <p>Substitution, partielle Integration, LIATE-Regel, Partialbruchzerlegung</p>
            <a href="/assets/pdfs/Integral_2_2.pdf" class="btn-small btn-preview" target="_blank">Vorschau</a>
            <a href="/assets/pdfs/Integral_2_2.pdf" class="btn-small btn-download" download>PDF herunterladen</a>
        </div>
        
        <div class="material-card integral" data-category="integralrechnung">
            <h4>📙 Hauptsatz & Flächen</h4>
            <p>Hauptsatz, bestimmte Integrale, Flächenberechnung zwischen Graphen</p>
            <a href="/assets/pdfs/Integral_2_3.pdf" class="btn-small btn-preview" target="_blank">Vorschau</a>
            <a href="/assets/pdfs/Integral_2_3.pdf" class="btn-small btn-download" download>PDF herunterladen</a>
        </div>
        
        <div class="material-card integral" data-category="integralrechnung">
            <h4>📕 Flächen & Rotationsvolumen</h4>
            <p>Flächenberechnung mit Integrationstechniken, Rotationskörper um x- und y-Achse, Volumen- und Massenberechnung</p>
            <a href="/assets/pdfs/Integral_2_4.pdf" class="btn-small btn-preview" target="_blank">Vorschau</a>
            <a href="/assets/pdfs/Integral_2_4.pdf" class="btn-small btn-download" download>PDF herunterladen</a>
        </div>
    </div>
    
    <a href="/teaching/" class="back-link">← Zurück zur Übersicht</a>

    <script>
        // Suchfunktion implementieren
        document.addEventListener('DOMContentLoaded', function() {
            const searchInput = document.getElementById('materialSearch');
            const categoryFilter = document.getElementById('categoryFilter');
            const materialCards = document.querySelectorAll('.material-card');
            
            function filterMaterials() {
                const searchTerm = searchInput.value.toLowerCase();
                const selectedCategory = categoryFilter.value;
                
                let visibleCount = 0;
                
                materialCards.forEach(card => {
                    const title = card.querySelector('h4').textContent.toLowerCase();
                    const description = card.querySelector('p').textContent.toLowerCase();
                    const category = card.getAttribute('data-category');
                    
                    const matchesSearch = title.includes(searchTerm) || description.includes(searchTerm);
                    const matchesCategory = selectedCategory === 'all' || category === selectedCategory;
                    
                    if (matchesSearch && matchesCategory) {
                        card.style.display = 'block';
                        visibleCount++;
                    } else {
                        card.style.display = 'none';
                    }
                });
                
                // "Keine Ergebnisse"-Nachricht anzeigen/verstecken
                let noResultsMsg = document.querySelector('.no-results');
                if (visibleCount === 0) {
                    if (!noResultsMsg) {
                        noResultsMsg = document.createElement('div');
                        noResultsMsg.className = 'no-results';
                        noResultsMsg.textContent = 'Keine Materialien gefunden, die Ihren Suchkriterien entsprechen.';
                        document.querySelector('.materials-grid').appendChild(noResultsMsg);
                    }
                } else if (noResultsMsg) {
                    noResultsMsg.remove();
                }
            }
            
            // Event-Listener für Suchfeld und Filter
            searchInput.addEventListener('input', filterMaterials);
            categoryFilter.addEventListener('change', filterMaterials);
            
            // Responsive Verbesserungen - Button-Verhalten auf kleinen Bildschirmen
            function adjustButtonLayout() {
                const buttons = document.querySelectorAll('.btn-small');
                if (window.innerWidth <= 480) {
                    buttons.forEach(btn => {
                        btn.style.display = 'block';
                        btn.style.margin = '0.5rem 0';
                    });
                } else {
                    buttons.forEach(btn => {
                        btn.style.display = 'inline-block';
                        btn.style.margin = '0 0.5rem 0.5rem 0';
                    });
                }
            }
            
            // Initial anpassen und bei Fenstergrößenänderung
            adjustButtonLayout();
            window.addEventListener('resize', adjustButtonLayout);
        });
    </script>
</body>
</html>