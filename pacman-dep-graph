# !/bin/bash
#
# Copyright (C) 2022 Vincil Lau
#
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation, either version 3 of the License, or
# (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program. If not, see <https://www.gnu.org/licenses/>.

LANG='en_US.UTF-8'

echo 'digraph pacman {'

for i in $(pacman -Qq); do
    i_id=$(echo $i | sed 's/-/_/g')
    echo "    ${i_id} [label=\"$i\"];"
done

for i in $(pacman -Qq); do
    i_id=$(echo $i | sed 's/-/_/g')
    required_by=$(pacman -Qi $i | grep 'Required By' | grep -v 'None' |
        awk '{$1="";$2="";$3="";print $0}')
    if [ -z "${required_by}" ]; then
        continue
    fi
    for j in ${required_by}; do
        j_id=$(echo $j | sed 's/-/_/g')
        echo "    ${j_id} -> ${i_id};"
    done
done

echo '}'
