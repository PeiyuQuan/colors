mkdir -p "$HOME/.config/edm"

sed \
  -e '/^courier=/c\courier=-adobe-courier-(medium,bold)-(r,o)-normal--*-(80,100,120,140,160,180,200,240,280,320,360,420,480,600,720)-75-75-m-*-iso8859-1' \
  -e '/^helvetica=/c\helvetica=-adobe-helvetica-(medium,bold)-(r,o)-normal--*-(80,100,120,140,160,180,200,240,280,320,360,420,480,600,720)-75-75-p-*-iso8859-1' \
  "$EDMFILES/fonts.list" > "$HOME/.config/edm/fonts-adobe.list"

export EDMFONTFILE="$HOME/.config/edm/fonts-adobe.list"
