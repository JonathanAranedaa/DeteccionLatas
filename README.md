# Detección de Latas con MLP

## Descripción
Clasificación binaria (Latas / No Latas) mediante una MLP en PyTorch.

## Dataset
- Fuente: (https://drive.google.com/file/d/1k3xNICLnAYv-mA90u3eP6qNjuJ_otsel/view?usp=sharing)
- Estructura esperada:
  Dataset/
    train/Latas/
    train/No_Latas/
    valid/...
    test/...
- Preprocesamiento: redimensionado a 64×64, normalización ImageNet.

## Configuración óptima encontrada
| Parámetro      | Valor |
|----------------|-------|
| Épocas         | 20    |
| LR             | 1e-3  |
| Batch Size     | 64    |
| Activación     | ReLU  |
| Loss           | CrossEntropy |
| Regularización | Dropout (0.5/0.4/0.3) + BN + WD 1e-4 |

## Cómo ejecutar
1. Clonar repo.
2. Instalar dependencias: `pip install torch torchvision matplotlib seaborn scikit-learn pandas`
3. Descargar dataset y colocarlo como se indica arriba.
4. Abrir el notebook o ejecutar el script de entrenamiento (si lo incluyes).

## Resultados finales
- Accuracy en validación: 78.01%
- F1-Score en validación: 0.8564
- Accuracy en test: 76.07%

## Predicción sobre una imagen
Ejecuta la última celda del notebook (código con el selector de archivos).
