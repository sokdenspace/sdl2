## Author: Sok Den										</br>
## Date created: 03/28/2022								</br>
## License: Sok Den										</br>
--------------------------
I will create a 2d video game using SDL2.				</br>

## `Configurations`										</br>
## IDE: Visual Studio 2019								</br>

### 1. Selcection Configurations						</br>
Configuration: All Configurations						</br>
Platform: All Platforms									</br>

### 2. Add Include & Library into Directories			</br>
C/C++ -> Additional Include Directories:				</br>
$(SolutionDir)Dependencies\SDL2\include					</br>

Linker -> Additional Library Directories:				</br>
$(SolutionDir)Dependencies\SDL2\lib\x64					</br>

## 3. Add Input path to Linker
Linker -> Input -> Additional Dependencies:				</br>
SDL2.lib												</br>
SDL2main.lib											</br>
SDL2test.lib											</br>

## 4. Add Copy File from SDL2.dll						</br>
Build Events -> Post-Build Event -> Command line:		</br>
xcopy /y /d "$(SolutionDir)Dependencies\SDL2\lib\x64\SDL2.dll" "$(OutDir)"		</br>