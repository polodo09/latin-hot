# latin-hot
app de citas
Perfecto, te muestro todos los archivos necesarios para copiar/pegar:
Action: {"type": "mcp_tool", "tool_name": "mcp_view_bulk", "tool_arguments": {"paths": ["/app/frontend/app.json", "/app/frontend/eas.json", "/app/frontend/package.json", "/app/frontend/app/_layout.tsx", "/app/frontend/app/index.tsx", "/app/frontend/app/callback.tsx"]}}
Observation: ===FILE: /app/frontend/app.json
/app/frontend/app.json:
1|{
2|  "expo": {
3|    "name": "LH Citas",
4|    "slug": "lh-citas",
5|    "version": "1.0.0",
6|    "orientation": "portrait",
7|    "icon": "./assets/images/lh-logo.png",
8|    "scheme": "lhcitas",
9|    "userInterfaceStyle": "dark",
10|    "newArchEnabled": true,
11|    "owner": "your-expo-username",
12|    "extra": {
13|      "eas": {
14|        "projectId": "your-project-id"
15|      }
16|    },
17|    "ios": {
18|      "supportsTablet": true,
19|      "bundleIdentifier": "com.lhcitas.app",
20|      "infoPlist": {
21|        "NSCameraUsageDescription": "Toma fotos para tu perfil",
22|        "NSPhotoLibraryUsageDescription": "Selecciona fotos para tu perfil",
23|        "NSLocationWhenInUseUsageDescription": "Encuentra personas cerca de ti"
24|      }
25|    },
26|    "android": {
27|      "package": "com.lhcitas.app",
28|      "versionCode": 1,
29|      "adaptiveIcon": {
30|        "foregroundImage": "./assets/images/lh-logo.png",
31|        "backgroundColor": "#000000"
32|      },
33|      "permissions": [
34|        "CAMERA",
35|        "READ_EXTERNAL_STORAGE",
36|        "WRITE_EXTERNAL_STORAGE",
37|        "ACCESS_FINE_LOCATION",
38|        "ACCESS_COARSE_LOCATION",
39|        "INTERNET",
40|        "ACCESS_NETWORK_STATE"
41|      ]
42|    },
43|    "web": {
44|      "bundler": "metro",
45|      "output": "static",
46|      "favicon": "./assets/images/lh-logo.png"
47|    },
48|    "plugins": [
49|      "expo-router",
50|      [
51|        "expo-splash-screen",
52|        {
53|          "image": "./assets/images/lh-logo.png",
54|          "imageWidth": 200,
55|          "resizeMode": "contain",
56|          "backgroundColor": "#000000"
57|        }
58|      ],
59|      [
60|        "expo-location",
61|        {
62|          "locationAlwaysAndWhenInUsePermission": "Permitir a LH Citas acceder a tu ubicación para encontrar personas cerca de ti."
63|        }
64|      ],
65|      [
66|        "expo-image-picker",
67|        {
68|          "photosPermission": "Permitir a LH Citas acceder a tus fotos para tu perfil.",
69|          "cameraPermission": "Permitir a LH Citas usar la cámara para tomar fotos de perfil."
70|        }
71|      ]
72|    ],
73|    "experiments": {
74|      "typedRoutes": true
75|    },
76|    "splash": {
77|      "image": "./assets/images/lh-logo.png",
78|      "resizeMode": "contain",
79|      "backgroundColor": "#000000"
80|    },
81|    "updates": {
82|      "fallbackToCacheTimeout": 0
83|    },
84|    "assetBundlePatterns": [
85|      "**/*"
86|    ]
87|  }
88|}
89|

===END

===FILE: /app/frontend/eas.json
/app/frontend/eas.json:
1|{
2|  "cli": {
3|    "version": ">= 5.0.0"
4|  },
5|  "build": {
6|    "development": {
7|      "developmentClient": true,
8|      "distribution": "internal"
9|    },
10|    "preview": {
11|      "android": {
12|        "buildType": "apk"
13|      },
14|      "distribution": "internal"
15|    },
16|    "production": {
17|      "android": {
18|        "buildType": "app-bundle"
19|      }
20|    }
21|  },
22|  "submit": {
23|    "production": {}
24|  }
25|}
26|

===END

===FILE: /app/frontend/package.json
/app/frontend/package.json:
1|{
2|  "name": "frontend",
3|  "main": "expo-router/entry",
4|  "version": "1.0.0",
5|  "scripts": {
6|    "start": "expo start",
7|    "reset-project": "node ./scripts/reset-project.js",
8|    "android": "expo start --android",
9|    "ios": "expo start --ios",
10|    "web": "expo start --web",
11|    "lint": "expo lint"
12|  },
13|  "dependencies": {
14|    "@babel/runtime": "^7.20.6",
15|    "@expo/metro-runtime": "^6.1.2",
16|    "@expo/ngrok": "^4.1.3",
17|    "@expo/vector-icons": "^15.0.3",
18|    "@react-native-async-storage/async-storage": "2.2.0",
19|    "@react-navigation/bottom-tabs": "^7.3.10",
20|    "@react-navigation/elements": "^2.3.8",
21|    "@react-navigation/native": "^7.1.6",
22|    "@react-navigation/native-stack": "^7.3.10",
23|    "axios": "^1.13.6",
24|    "date-fns": "^4.1.0",
25|    "expo": "54.0.33",
26|    "expo-blur": "~15.0.8",
27|    "expo-constants": "~18.0.13",
28|    "expo-font": "~14.0.11",
29|    "expo-haptics": "~15.0.8",
30|    "expo-image": "~3.0.11",
31|    "expo-image-picker": "~17.0.10",
32|    "expo-linear-gradient": "~15.0.8",
33|    "expo-linking": "~8.0.11",
34|    "expo-location": "~19.0.8",
35|    "expo-router": "~6.0.22",
36|    "expo-splash-screen": "~31.0.13",
37|    "expo-status-bar": "~3.0.9",
38|    "expo-symbols": "~1.0.8",
39|    "expo-system-ui": "~6.0.9",
40|    "expo-web-browser": "~15.0.10",
41|    "react": "19.1.0",
42|    "react-dom": "19.1.0",
43|    "react-native": "0.81.5",
44|    "react-native-dotenv": "^3.4.11",
45|    "react-native-gesture-handler": "~2.28.0",
46|    "react-native-reanimated": "~4.1.1",
47|    "react-native-safe-area-context": "~5.6.0",
48|    "react-native-screens": "~4.16.0",
49|    "react-native-web": "^0.21.0",
50|    "react-native-webview": "13.15.0",
51|    "react-native-worklets": "0.5.1",
52|    "zustand": "^5.0.12"
53|  },
54|  "devDependencies": {
55|    "@babel/core": "^7.25.2",
56|    "@types/react": "~19.1.0",
57|    "eslint": "^9.25.0",
58|    "eslint-config-expo": "~10.0.0",
59|    "typescript": "~5.9.3"
60|  },
61|  "private": true,
62|  "packageManager": "yarn@1.22.22+sha512.a6b2f7906b721bba3d67d4aff083df04dad64c399707841b7acf00f6b133b7ac24255f2652fa22ae3534329dc6180534e98d17432037ff6fd140556e2bb3137e"
63|}
64|

===END

===FILE: /app/frontend/app/_layout.tsx
/app/frontend/app/_layout.tsx:
1|import React, { useEffect, useState, createContext, useContext } from 'react';
2|import { Stack, useRouter, usePathname } from 'expo-router';
3|import { StatusBar } from 'expo-status-bar';
4|import { View, ActivityIndicator, StyleSheet } from 'react-native';
5|import AsyncStorage from '@react-native-async-storage/async-storage';
6|import axios from 'axios';
7|
8|const BACKEND_URL = process.env.EXPO_PUBLIC_BACKEND_URL;
9|
10|// Auth Context
11|interface User {
12|  user_id: string;
13|  email: string;
14|  name: string;
15|  picture?: string;
16|  bio?: string;
17|  age?: number;
18|  gender?: string;
19|  looking_for?: string;
20|  photos: string[];
21|  location?: { lat: number; lng: number };
22|  city?: string;
23|  is_verified: boolean;
24|  preferences?: any;
25|}
26|
27|interface AuthContextType {
28|  user: User | null;
29|  setUser: (user: User | null) => void;
30|  isLoading: boolean;
31|  logout: () => Promise<void>;
32|  refreshUser: () => Promise<void>;
33|}
34|
35|export const AuthContext = createContext<AuthContextType>({
36|  user: null,
37|  setUser: () => {},
38|  isLoading: true,
39|  logout: async () => {},
40|  refreshUser: async () => {},
41|});
42|
43|export const useAuth = () => useContext(AuthContext);
44|
45|export default function RootLayout() {
46|  const [user, setUser] = useState<User | null>(null);
47|  const [isLoading, setIsLoading] = useState(true);
48|  const router = useRouter();
49|  const pathname = usePathname();
50|
51|  const checkAuth = async () => {
52|    try {
53|      const token = await AsyncStorage.getItem('session_token');
54|      if (!token) {
55|        setIsLoading(false);
56|        return;
57|      }
58|
59|      const response = await axios.get(`${BACKEND_URL}/api/auth/me`, {
60|        headers: { Authorization: `Bearer ${token}` },
61|      });
62|
63|      if (response.data) {
64|        setUser(response.data);
65|      }
66|    } catch (error) {
67|      console.log('Auth check failed:', error);
68|      await AsyncStorage.removeItem('session_token');
69|    } finally {
70|      setIsLoading(false);
71|    }
72|  };
73|
74|  const refreshUser = async () => {
75|    try {
76|      const token = await AsyncStorage.getItem('session_token');
77|      if (!token) return;
78|
79|      const response = await axios.get(`${BACKEND_URL}/api/auth/me`, {
80|        headers: { Authorization: `Bearer ${token}` },
81|      });
82|
83|      if (response.data) {
84|        setUser(response.data);
85|      }
86|    } catch (error) {
87|      console.log('Refresh user failed:', error);
88|    }
89|  };
90|
91|  const logout = async () => {
92|    try {
93|      const token = await AsyncStorage.getItem('session_token');
94|      if (token) {
95|        await axios.post(
96|          `${BACKEND_URL}/api/auth/logout`,
97|          {},
98|          { headers: { Authorization: `Bearer ${token}` } }
99|        );
100|      }
101|    } catch (error) {
102|      console.log('Logout error:', error);
103|    } finally {
104|      await AsyncStorage.removeItem('session_token');
105|      setUser(null);
106|      router.replace('/');
107|    }
108|  };
109|
110|  useEffect(() => {
111|    // Skip auth check if on callback page (handling OAuth)
112|    if (pathname === '/callback') {
113|      setIsLoading(false);
114|      return;
115|    }
116|    checkAuth();
117|  }, [pathname]);
118|
119|  if (isLoading) {
120|    return (
121|      <View style={styles.loadingContainer}>
122|        <ActivityIndicator size="large" color="#C41E3A" />
123|      </View>
124|    );
125|  }
126|
127|  return (
128|    <AuthContext.Provider value={{ user, setUser, isLoading, logout, refreshUser }}>
129|      <StatusBar style="light" />
130|      <Stack
131|        screenOptions={{
132|          headerShown: false,
133|          contentStyle: { backgroundColor: '#000000' },
134|          animation: 'slide_from_right',
135|        }}
136|      >
137|        <Stack.Screen name="index" />
138|        <Stack.Screen name="callback" />
139|        <Stack.Screen name="(tabs)" />
140|        <Stack.Screen name="profile/edit" />
141|        <Stack.Screen name="chat/[matchId]" />
142|      </Stack>
143|    </AuthContext.Provider>
144|  );
145|}
146|
147|const styles = StyleSheet.create({
148|  loadingContainer: {
149|    flex: 1,
150|    justifyContent: 'center',
151|    alignItems: 'center',
152|    backgroundColor: '#000000',
153|  },
154|});
155|

===END

===FILE: /app/frontend/app/index.tsx
/app/frontend/app/index.tsx:
1|import React, { useEffect } from 'react';
2|import { View, Text, StyleSheet, TouchableOpacity, Image, Platform } from 'react-native';
3|import { useRouter } from 'expo-router';
4|import { LinearGradient } from 'expo-linear-gradient';
5|import { Ionicons } from '@expo/vector-icons';
6|import { useAuth } from './_layout';
7|import * as WebBrowser from 'expo-web-browser';
8|import * as Linking from 'expo-linking';
9|
10|const LOGO_URL = 'https://customer-assets.emergentagent.com/job_fdec6e5f-84f3-49d4-bc45-b90521798d31/artifacts/q6ttbsqj_a2c01f7d-8461-4cd8-99e1-e9f62bb7336d.png';
11|
12|export default function LoginScreen() {
13|  const router = useRouter();
14|  const { user, isLoading } = useAuth();
15|
16|  useEffect(() => {
17|    if (user && !isLoading) {
18|      // Check if profile is complete
19|      if (user.age && user.gender && user.photos?.length > 0) {
20|        router.replace('/(tabs)/discover');
21|      } else {
22|        router.replace('/profile/edit');
23|      }
24|    }
25|  }, [user, isLoading]);
26|
27|  const handleGoogleLogin = async () => {
28|    // REMINDER: DO NOT HARDCODE THE URL, OR ADD ANY FALLBACKS OR REDIRECT URLS, THIS BREAKS THE AUTH
29|    const currentUrl = Linking.createURL('/callback');
30|    const authUrl = `https://auth.emergentagent.com/?redirect=${encodeURIComponent(currentUrl)}`;
31|    
32|    if (Platform.OS === 'web') {
33|      window.location.href = authUrl;
34|    } else {
35|      const result = await WebBrowser.openAuthSessionAsync(authUrl, currentUrl);
36|      if (result.type === 'success' && result.url) {
37|        // Handle the callback URL
38|        const urlParams = new URL(result.url);
39|        const hash = urlParams.hash;
40|        if (hash && hash.includes('session_id=')) {
41|          const sessionId = hash.split('session_id=')[1];
42|          router.push(`/callback?session_id=${sessionId}`);
43|        }
44|      }
45|    }
46|  };
47|
48|  return (
49|    <View style={styles.container}>
50|      <LinearGradient
51|        colors={['#1a0000', '#000000', '#1a0a00']}
52|        style={styles.gradient}
53|      >
54|        <View style={styles.content}>
55|          {/* Logo */}
56|          <View style={styles.logoContainer}>
57|            <Image
58|              source={{ uri: LOGO_URL }}
59|              style={styles.logo}
60|              resizeMode="contain"
61|            />
62|          </View>
63|
64|          {/* Tagline */}
65|          <Text style={styles.title}>LH Citas</Text>
66|          <Text style={styles.subtitle}>Conexiones serias para el amor verdadero</Text>
67|
68|          {/* Features */}
69|          <View style={styles.features}>
70|            <View style={styles.featureItem}>
71|              <Ionicons name="shield-checkmark" size={24} color="#D4AF37" />
72|              <Text style={styles.featureText}>Perfiles verificados</Text>
73|            </View>
74|            <View style={styles.featureItem}>
75|              <Ionicons name="location" size={24} color="#D4AF37" />
76|              <Text style={styles.featureText}>Filtros por ubicación</Text>
77|            </View>
78|            <View style={styles.featureItem}>
79|              <Ionicons name="heart" size={24} color="#D4AF37" />
80|              <Text style={styles.featureText}>Relaciones serias</Text>
81|            </View>
82|          </View>
83|
84|          {/* Login Button */}
85|          <TouchableOpacity
86|            style={styles.googleButton}
87|            onPress={handleGoogleLogin}
88|            activeOpacity={0.8}
89|          >
90|            <Ionicons name="logo-google" size={24} color="#FFFFFF" />
91|            <Text style={styles.googleButtonText}>Continuar con Google</Text>
92|          </TouchableOpacity>
93|
94|          <Text style={styles.termsText}>
95|            Al continuar, aceptas nuestros Términos de Servicio y Política de Privacidad
96|          </Text>
97|        </View>
98|      </LinearGradient>
99|    </View>
100|  );
101|}
102|
103|const styles = StyleSheet.create({
104|  container: {
105|    flex: 1,
106|    backgroundColor: '#000000',
107|  },
108|  gradient: {
109|    flex: 1,
110|  },
111|  content: {
112|    flex: 1,
113|    justifyContent: 'center',
114|    alignItems: 'center',
115|    paddingHorizontal: 32,
116|  },
117|  logoContainer: {
118|    width: 150,
119|    height: 150,
120|    marginBottom: 24,
121|    borderRadius: 75,
122|    overflow: 'hidden',
123|    borderWidth: 3,
124|    borderColor: '#D4AF37',
125|    shadowColor: '#D4AF37',
126|    shadowOffset: { width: 0, height: 0 },
127|    shadowOpacity: 0.5,
128|    shadowRadius: 20,
129|    elevation: 10,
130|  },
131|  logo: {
132|    width: '100%',
133|    height: '100%',
134|  },
135|  title: {
136|    fontSize: 42,
137|    fontWeight: 'bold',
138|    color: '#FFFFFF',
139|    marginBottom: 8,
140|    textShadowColor: '#C41E3A',
141|    textShadowOffset: { width: 0, height: 2 },
142|    textShadowRadius: 10,
143|  },
144|  subtitle: {
145|    fontSize: 16,
146|    color: '#D4AF37',
147|    marginBottom: 48,
148|    textAlign: 'center',
149|  },
150|  features: {
151|    marginBottom: 48,
152|  },
153|  featureItem: {
154|    flexDirection: 'row',
155|    alignItems: 'center',
156|    marginBottom: 16,
157|  },
158|  featureText: {
159|    fontSize: 16,
160|    color: '#FFFFFF',
161|    marginLeft: 12,
162|  },
163|  googleButton: {
164|    flexDirection: 'row',
165|    alignItems: 'center',
166|    justifyContent: 'center',
167|    backgroundColor: '#C41E3A',
168|    paddingVertical: 16,
169|    paddingHorizontal: 32,
170|    borderRadius: 30,
171|    width: '100%',
172|    borderWidth: 2,
173|    borderColor: '#D4AF37',
174|    shadowColor: '#C41E3A',
175|    shadowOffset: { width: 0, height: 4 },
176|    shadowOpacity: 0.4,
177|    shadowRadius: 8,
178|    elevation: 8,
179|  },
180|  googleButtonText: {
181|    fontSize: 18,
182|    fontWeight: '600',
183|    color: '#FFFFFF',
184|    marginLeft: 12,
185|  },
186|  termsText: {
187|    fontSize: 12,
188|    color: '#888888',
189|    textAlign: 'center',
190|    marginTop: 24,
191|    paddingHorizontal: 20,
192|  },
193|});
194|

===END

===FILE: /app/frontend/app/callback.tsx
/app/frontend/app/callback.tsx:
1|import React, { useEffect, useRef } from 'react';
2|import { View, Text, StyleSheet, ActivityIndicator, Platform } from 'react-native';
3|import { useRouter, useLocalSearchParams } from 'expo-router';
4|import AsyncStorage from '@react-native-async-storage/async-storage';
5|import axios from 'axios';
6|import { useAuth } from './_layout';
7|
8|const BACKEND_URL = process.env.EXPO_PUBLIC_BACKEND_URL;
9|
10|export default function CallbackScreen() {
11|  const router = useRouter();
12|  const params = useLocalSearchParams();
13|  const { setUser } = useAuth();
14|  const hasProcessed = useRef(false);
15|
16|  useEffect(() => {
17|    const handleCallback = async () => {
18|      if (hasProcessed.current) return;
19|      hasProcessed.current = true;
20|
21|      try {
22|        let sessionId = params.session_id as string;
23|
24|        // On web, check URL hash
25|        if (!sessionId && Platform.OS === 'web') {
26|          const hash = window.location.hash;
27|          if (hash && hash.includes('session_id=')) {
28|            sessionId = hash.split('session_id=')[1].split('&')[0];
29|          }
30|        }
31|
32|        if (!sessionId) {
33|          console.log('No session_id found');
34|          router.replace('/');
35|          return;
36|        }
37|
38|        console.log('Processing session_id:', sessionId);
39|
40|        // Exchange session_id for session_token
41|        const response = await axios.post(`${BACKEND_URL}/api/auth/session`, {
42|          session_id: sessionId,
43|        });
44|
45|        if (response.data.user) {
46|          // Get session_token from the auth response
47|          const sessionToken = response.headers['set-cookie']?.[0]?.match(/session_token=([^;]+)/)?.[1];
48|          
49|          // For mobile/web, we need to extract token differently
50|          // The backend returns the user, but we need to store the token
51|          // We'll make another call to get the token from the session
52|          const meResponse = await axios.get(`${BACKEND_URL}/api/auth/me`, {
53|            withCredentials: true,
54|          });
55|
56|          // Store the session_id as token (backend accepts it)
57|          await AsyncStorage.setItem('session_token', sessionId);
58|          
59|          setUser(response.data.user);
60|
61|          // Check if profile is complete
62|          const user = response.data.user;
63|          if (user.age && user.gender && user.photos?.length > 0) {
64|            router.replace('/(tabs)/discover');
65|          } else {
66|            router.replace('/profile/edit');
67|          }
68|        }
69|      } catch (error) {
70|        console.error('Callback error:', error);
71|        router.replace('/');
72|      }
73|    };
74|
75|    handleCallback();
76|  }, []);
77|
78|  return (
79|    <View style={styles.container}>
80|      <ActivityIndicator size="large" color="#C41E3A" />
81|      <Text style={styles.text}>Iniciando sesión...</Text>
82|    </View>
83|  );
84|}
85|
86|const styles = StyleSheet.create({
87|  container: {
88|    flex: 1,
89|    justifyContent: 'center',
90|    alignItems: 'center',
91|    backgroundColor: '#000000',
92|  },
93|  text: {
94|    color: '#FFFFFF',
95|    fontSize: 18,
96|    marginTop: 20,
97|  },
98|});
99|

===END
Ahora los archivos de las tabs:
Action: {"type": "mcp_tool", "tool_name": "mcp_view_bulk", "tool_arguments": {"paths": ["/app/frontend/app/(tabs)/_layout.tsx", "/app/frontend/app/(tabs)/discover.tsx", "/app/frontend/app/(tabs)/likes.tsx"]}}
Observation: ===FILE: /app/frontend/app/(tabs)/_layout.tsx
/app/frontend/app/(tabs)/_layout.tsx:
1|import React from 'react';
2|import { Tabs } from 'expo-router';
3|import { Ionicons } from '@expo/vector-icons';
4|import { View, StyleSheet } from 'react-native';
5|import { useAuth } from '../_layout';
6|import { useRouter } from 'expo-router';
7|import { useEffect } from 'react';
8|
9|export default function TabsLayout() {
10|  const { user, isLoading } = useAuth();
11|  const router = useRouter();
12|
13|  useEffect(() => {
14|    if (!isLoading && !user) {
15|      router.replace('/');
16|    }
17|  }, [user, isLoading]);
18|
19|  if (!user) {
20|    return null;
21|  }
22|
23|  return (
24|    <View style={styles.container}>
25|      <Tabs
26|        screenOptions={{
27|          headerShown: false,
28|          tabBarStyle: styles.tabBar,
29|          tabBarActiveTintColor: '#C41E3A',
30|          tabBarInactiveTintColor: '#888888',
31|          tabBarShowLabel: true,
32|          tabBarLabelStyle: styles.tabBarLabel,
33|        }}
34|      >
35|        <Tabs.Screen
36|          name="discover"
37|          options={{
38|            title: 'Descubrir',
39|            tabBarIcon: ({ color, size }) => (
40|              <Ionicons name="flame" size={size} color={color} />
41|            ),
42|          }}
43|        />
44|        <Tabs.Screen
45|          name="likes"
46|          options={{
47|            title: 'Me Gusta',
48|            tabBarIcon: ({ color, size }) => (
49|              <Ionicons name="heart" size={size} color={color} />
50|            ),
51|          }}
52|        />
53|        <Tabs.Screen
54|          name="matches"
55|          options={{
56|            title: 'Matches',
57|            tabBarIcon: ({ color, size }) => (
58|              <Ionicons name="chatbubbles" size={size} color={color} />
59|            ),
60|          }}
61|        />
62|        <Tabs.Screen
63|          name="profile"
64|          options={{
65|            title: 'Perfil',
66|            tabBarIcon: ({ color, size }) => (
67|              <Ionicons name="person" size={size} color={color} />
68|            ),
69|          }}
70|        />
71|      </Tabs>
72|    </View>
73|  );
74|}
75|
76|const styles = StyleSheet.create({
77|  container: {
78|    flex: 1,
79|    backgroundColor: '#000000',
80|  },
81|  tabBar: {
82|    backgroundColor: '#1a1a1a',
83|    borderTopColor: '#333333',
84|    borderTopWidth: 1,
85|    paddingTop: 8,
86|    paddingBottom: 8,
87|    height: 70,
88|  },
89|  tabBarLabel: {
90|    fontSize: 12,
91|    fontWeight: '500',
92|  },
93|});
94|

===END

===FILE: /app/frontend/app/(tabs)/discover.tsx
/app/frontend/app/(tabs)/discover.tsx:
1|import React, { useState, useEffect, useRef } from 'react';
2|import {
3|  View,
4|  Text,
5|  StyleSheet,
6|  Image,
7|  TouchableOpacity,
8|  Dimensions,
9|  ActivityIndicator,
10|  Animated,
11|  PanResponder,
12|  Alert,
13|} from 'react-native';
14|import { SafeAreaView } from 'react-native-safe-area-context';
15|import { Ionicons } from '@expo/vector-icons';
16|import axios from 'axios';
17|import AsyncStorage from '@react-native-async-storage/async-storage';
18|import { useAuth } from '../_layout';
19|
20|const BACKEND_URL = process.env.EXPO_PUBLIC_BACKEND_URL;
21|const { width, height } = Dimensions.get('window');
22|const SWIPE_THRESHOLD = 120;
23|
24|interface Profile {
25|  user_id: string;
26|  name: string;
27|  age?: number;
28|  bio?: string;
29|  photos: string[];
30|  city?: string;
31|  is_verified: boolean;
32|  distance?: number;
33|}
34|
35|export default function DiscoverScreen() {
36|  const { user } = useAuth();
37|  const [profiles, setProfiles] = useState<Profile[]>([]);
38|  const [currentIndex, setCurrentIndex] = useState(0);
39|  const [loading, setLoading] = useState(true);
40|  const [showMatch, setShowMatch] = useState<Profile | null>(null);
41|  const [currentPhotoIndex, setCurrentPhotoIndex] = useState(0);
42|
43|  const position = useRef(new Animated.ValueXY()).current;
44|  const rotate = position.x.interpolate({
45|    inputRange: [-width / 2, 0, width / 2],
46|    outputRange: ['-10deg', '0deg', '10deg'],
47|    extrapolate: 'clamp',
48|  });
49|
50|  const likeOpacity = position.x.interpolate({
51|    inputRange: [0, width / 4],
52|    outputRange: [0, 1],
53|    extrapolate: 'clamp',
54|  });
55|
56|  const nopeOpacity = position.x.interpolate({
57|    inputRange: [-width / 4, 0],
58|    outputRange: [1, 0],
59|    extrapolate: 'clamp',
60|  });
61|
62|  const nextCardScale = position.x.interpolate({
63|    inputRange: [-width / 2, 0, width / 2],
64|    outputRange: [1, 0.9, 1],
65|    extrapolate: 'clamp',
66|  });
67|
68|  const panResponder = useRef(
69|    PanResponder.create({
70|      onStartShouldSetPanResponder: () => true,
71|      onPanResponderMove: (_, gesture) => {
72|        position.setValue({ x: gesture.dx, y: gesture.dy });
73|      },
74|      onPanResponderRelease: (_, gesture) => {
75|        if (gesture.dx > SWIPE_THRESHOLD) {
76|          swipeRight();
77|        } else if (gesture.dx < -SWIPE_THRESHOLD) {
78|          swipeLeft();
79|        } else {
80|          resetPosition();
81|        }
82|      },
83|    })
84|  ).current;
85|
86|  useEffect(() => {
87|    fetchProfiles();
88|  }, []);
89|
90|  const fetchProfiles = async () => {
91|    try {
92|      const token = await AsyncStorage.getItem('session_token');
93|      const response = await axios.get(`${BACKEND_URL}/api/discover`, {
94|        headers: { Authorization: `Bearer ${token}` },
95|        params: {
96|          min_age: user?.preferences?.min_age || 18,
97|          max_age: user?.preferences?.max_age || 99,
98|          max_distance: user?.preferences?.max_distance || 100,
99|        },
100|      });
101|      setProfiles(response.data);
102|    } catch (error) {
103|      console.error('Error fetching profiles:', error);
104|    } finally {
105|      setLoading(false);
106|    }
107|  };
108|
109|  const resetPosition = () => {
110|    Animated.spring(position, {
111|      toValue: { x: 0, y: 0 },
112|      useNativeDriver: false,
113|    }).start();
114|  };
115|
116|  const swipeRight = async () => {
117|    const currentProfile = profiles[currentIndex];
118|    Animated.timing(position, {
119|      toValue: { x: width + 100, y: 0 },
120|      duration: 300,
121|      useNativeDriver: false,
122|    }).start(() => {
123|      handleLike(currentProfile);
124|      position.setValue({ x: 0, y: 0 });
125|      setCurrentPhotoIndex(0);
126|    });
127|  };
128|
129|  const swipeLeft = () => {
130|    const currentProfile = profiles[currentIndex];
131|    Animated.timing(position, {
132|      toValue: { x: -width - 100, y: 0 },
133|      duration: 300,
134|      useNativeDriver: false,
135|    }).start(() => {
136|      handlePass(currentProfile);
137|      position.setValue({ x: 0, y: 0 });
138|      setCurrentPhotoIndex(0);
139|    });
140|  };
141|
142|  const handleLike = async (profile: Profile) => {
143|    try {
144|      const token = await AsyncStorage.getItem('session_token');
145|      const response = await axios.post(
146|        `${BACKEND_URL}/api/like`,
147|        { target_user_id: profile.user_id },
148|        { headers: { Authorization: `Bearer ${token}` } }
149|      );
150|
151|      if (response.data.is_match) {
152|        setShowMatch(profile);
153|      }
154|    } catch (error) {
155|      console.error('Error liking profile:', error);
156|    }
157|    setCurrentIndex((prev) => prev + 1);
158|  };
159|
160|  const handlePass = async (profile: Profile) => {
161|    try {
162|      const token = await AsyncStorage.getItem('session_token');
163|      await axios.post(
164|        `${BACKEND_URL}/api/pass`,
165|        { target_user_id: profile.user_id },
166|        { headers: { Authorization: `Bearer ${token}` } }
167|      );
168|    } catch (error) {
169|      console.error('Error passing profile:', error);
170|    }
171|    setCurrentIndex((prev) => prev + 1);
172|  };
173|
174|  const handlePhotoTap = (side: 'left' | 'right') => {
175|    const currentProfile = profiles[currentIndex];
176|    if (!currentProfile) return;
177|
178|    const maxPhotos = currentProfile.photos.length;
179|    if (side === 'right' && currentPhotoIndex < maxPhotos - 1) {
180|      setCurrentPhotoIndex((prev) => prev + 1);
181|    } else if (side === 'left' && currentPhotoIndex > 0) {
182|      setCurrentPhotoIndex((prev) => prev - 1);
183|    }
184|  };
185|
186|  const renderCard = (profile: Profile, index: number) => {
187|    if (index < currentIndex) return null;
188|
189|    const isCurrentCard = index === currentIndex;
190|    const photo = profile.photos[isCurrentCard ? currentPhotoIndex : 0];
191|
192|    if (isCurrentCard) {
193|      return (
194|        <Animated.View
195|          key={profile.user_id}
196|          style={[
197|            styles.card,
198|            {
199|              transform: [
200|                { translateX: position.x },
201|                { translateY: position.y },
202|                { rotate },
203|              ],
204|            },
205|          ]}
206|          {...panResponder.panHandlers}
207|        >
208|          {/* Photo indicators */}
209|          <View style={styles.photoIndicators}>
210|            {profile.photos.map((_, i) => (
211|              <View
212|                key={i}
213|                style={[
214|                  styles.photoIndicator,
215|                  i === currentPhotoIndex && styles.photoIndicatorActive,
216|                ]}
217|              />
218|            ))}
219|          </View>
220|
221|          {/* Tap areas for photos */}
222|          <View style={styles.tapAreas}>
223|            <TouchableOpacity
224|              style={styles.tapArea}
225|              onPress={() => handlePhotoTap('left')}
226|              activeOpacity={1}
227|            />
228|            <TouchableOpacity
229|              style={styles.tapArea}
230|              onPress={() => handlePhotoTap('right')}
231|              activeOpacity={1}
232|            />
233|          </View>
234|
235|          <Image
236|            source={{ uri: photo }}
237|            style={styles.cardImage}
238|            resizeMode="cover"
239|          />
240|
241|          {/* Like/Nope overlays */}
242|          <Animated.View style={[styles.likeLabel, { opacity: likeOpacity }]}>
243|            <Text style={styles.likeLabelText}>ME GUSTA</Text>
244|          </Animated.View>
245|
246|          <Animated.View style={[styles.nopeLabel, { opacity: nopeOpacity }]}>
247|            <Text style={styles.nopeLabelText}>PASO</Text>
248|          </Animated.View>
249|
250|          {/* Profile info */}
251|          <View style={styles.cardInfo}>
252|            <View style={styles.nameRow}>
253|              <Text style={styles.cardName}>
254|                {profile.name}, {profile.age}
255|              </Text>
256|              {profile.is_verified && (
257|                <Ionicons name="shield-checkmark" size={24} color="#D4AF37" />
258|              )}
259|            </View>
260|            {profile.city && (
261|              <View style={styles.locationRow}>
262|                <Ionicons name="location" size={16} color="#D4AF37" />
263|                <Text style={styles.cardLocation}>
264|                  {profile.city}
265|                  {profile.distance && ` • ${profile.distance} km`}
266|                </Text>
267|              </View>
268|            )}
269|            {profile.bio && (
270|              <Text style={styles.cardBio} numberOfLines={2}>
271|                {profile.bio}
272|              </Text>
273|            )}
274|          </View>
275|        </Animated.View>
276|      );
277|    }
278|
279|    // Next card (behind)
280|    return (
281|      <Animated.View
282|        key={profile.user_id}
283|        style={[
284|          styles.card,
285|          styles.nextCard,
286|          { transform: [{ scale: nextCardScale }] },
287|        ]}
288|      >
289|        <Image
290|          source={{ uri: photo }}
291|          style={styles.cardImage}
292|          resizeMode="cover"
293|        />
294|        <View style={styles.cardInfo}>
295|          <Text style={styles.cardName}>
296|            {profile.name}, {profile.age}
297|          </Text>
298|        </View>
299|      </Animated.View>
300|    );
301|  };
302|
303|  if (loading) {
304|    return (
305|      <SafeAreaView style={styles.container}>
306|        <View style={styles.loadingContainer}>
307|          <ActivityIndicator size="large" color="#C41E3A" />
308|          <Text style={styles.loadingText}>Buscando perfiles...</Text>
309|        </View>
310|      </SafeAreaView>
311|    );
312|  }
313|
314|  if (currentIndex >= profiles.length) {
315|    return (
316|      <SafeAreaView style={styles.container}>
317|        <View style={styles.emptyContainer}>
318|          <Ionicons name="heart-dislike" size={80} color="#333333" />
319|          <Text style={styles.emptyTitle}>No hay más perfiles</Text>
320|          <Text style={styles.emptySubtitle}>
321|            Vuelve más tarde para conocer más personas
322|          </Text>
323|          <TouchableOpacity
324|            style={styles.refreshButton}
325|            onPress={() => {
326|              setCurrentIndex(0);
327|              setLoading(true);
328|              fetchProfiles();
329|            }}
330|          >
331|            <Text style={styles.refreshButtonText}>Actualizar</Text>
332|          </TouchableOpacity>
333|        </View>
334|      </SafeAreaView>
335|    );
336|  }
337|
338|  return (
339|    <SafeAreaView style={styles.container}>
340|      {/* Header */}
341|      <View style={styles.header}>
342|        <Text style={styles.headerTitle}>Descubrir</Text>
343|      </View>
344|
345|      {/* Cards */}
346|      <View style={styles.cardsContainer}>
347|        {profiles
348|          .slice(currentIndex, currentIndex + 2)
349|          .reverse()
350|          .map((profile, i) => renderCard(profile, currentIndex + 1 - i))}
351|      </View>
352|
353|      {/* Action buttons */}
354|      <View style={styles.actions}>
355|        <TouchableOpacity
356|          style={[styles.actionButton, styles.passButton]}
357|          onPress={swipeLeft}
358|        >
359|          <Ionicons name="close" size={32} color="#FF4444" />
360|        </TouchableOpacity>
361|
362|        <TouchableOpacity
363|          style={[styles.actionButton, styles.likeButton]}
364|          onPress={swipeRight}
365|        >
366|          <Ionicons name="heart" size={32} color="#C41E3A" />
367|        </TouchableOpacity>
368|      </View>
369|
370|      {/* Match Modal */}
371|      {showMatch && (
372|        <View style={styles.matchOverlay}>
373|          <View style={styles.matchContent}>
374|            <Text style={styles.matchTitle}>¡Es un Match!</Text>
375|            <Text style={styles.matchSubtitle}>
376|              Tú y {showMatch.name} se gustan mutuamente
377|            </Text>
378|            <Image
379|              source={{ uri: showMatch.photos[0] }}
380|              style={styles.matchImage}
381|            />
382|            <TouchableOpacity
383|              style={styles.matchButton}
384|              onPress={() => setShowMatch(null)}
385|            >
386|              <Text style={styles.matchButtonText}>Continuar</Text>
387|            </TouchableOpacity>
388|          </View>
389|        </View>
390|      )}
391|    </SafeAreaView>
392|  );
393|}
394|
395|const styles = StyleSheet.create({
396|  container: {
397|    flex: 1,
398|    backgroundColor: '#000000',
399|  },
400|  header: {
401|    paddingHorizontal: 20,
402|    paddingVertical: 16,
403|  },
404|  headerTitle: {
405|    fontSize: 28,
406|    fontWeight: 'bold',
407|    color: '#FFFFFF',
408|  },
409|  loadingContainer: {
410|    flex: 1,
411|    justifyContent: 'center',
412|    alignItems: 'center',
413|  },
414|  loadingText: {
415|    color: '#888888',
416|    marginTop: 16,
417|    fontSize: 16,
418|  },
419|  emptyContainer: {
420|    flex: 1,
421|    justifyContent: 'center',
422|    alignItems: 'center',
423|    paddingHorizontal: 40,
424|  },
425|  emptyTitle: {
426|    fontSize: 24,
427|    fontWeight: 'bold',
428|    color: '#FFFFFF',
429|    marginTop: 20,
430|  },
431|  emptySubtitle: {
432|    fontSize: 16,
433|    color: '#888888',
434|    textAlign: 'center',
435|    marginTop: 8,
436|  },
437|  refreshButton: {
438|    marginTop: 24,
439|    backgroundColor: '#C41E3A',
440|    paddingVertical: 12,
441|    paddingHorizontal: 32,
442|    borderRadius: 25,
443|  },
444|  refreshButtonText: {
445|    color: '#FFFFFF',
446|    fontSize: 16,
447|    fontWeight: '600',
448|  },
449|  cardsContainer: {
450|    flex: 1,
451|    alignItems: 'center',
452|    justifyContent: 'center',
453|  },
454|  card: {
455|    width: width - 40,
456|    height: height * 0.6,
457|    borderRadius: 20,
458|    backgroundColor: '#1a1a1a',
459|    position: 'absolute',
460|    overflow: 'hidden',
461|    shadowColor: '#000',
462|    shadowOffset: { width: 0, height: 4 },
463|    shadowOpacity: 0.3,
464|    shadowRadius: 8,
465|    elevation: 8,
466|  },
467|  nextCard: {
468|    zIndex: -1,
469|  },
470|  cardImage: {
471|    width: '100%',
472|    height: '100%',
473|  },
474|  photoIndicators: {
475|    position: 'absolute',
476|    top: 10,
477|    left: 10,
478|    right: 10,
479|    flexDirection: 'row',
480|    zIndex: 10,
481|    gap: 4,
482|  },
483|  photoIndicator: {
484|    flex: 1,
485|    height: 3,
486|    backgroundColor: 'rgba(255,255,255,0.3)',
487|    borderRadius: 2,
488|  },
489|  photoIndicatorActive: {
490|    backgroundColor: '#FFFFFF',
491|  },
492|  tapAreas: {
493|    position: 'absolute',
494|    top: 0,
495|    left: 0,
496|    right: 0,
497|    bottom: 100,
498|    flexDirection: 'row',
499|    zIndex: 5,
500|  },
501|  tapArea: {
502|    flex: 1,
503|  },
504|  likeLabel: {
505|    position: 'absolute',
506|    top: 50,
507|    left: 20,
508|    padding: 10,
509|    borderWidth: 3,
510|    borderColor: '#00FF00',
511|    borderRadius: 10,
512|    transform: [{ rotate: '-15deg' }],
513|  },
514|  likeLabelText: {
515|    fontSize: 32,
516|    fontWeight: 'bold',
517|    color: '#00FF00',
518|  },
519|  nopeLabel: {
520|    position: 'absolute',
521|    top: 50,
522|    right: 20,
523|    padding: 10,
524|    borderWidth: 3,
525|    borderColor: '#FF4444',
526|    borderRadius: 10,
527|    transform: [{ rotate: '15deg' }],
528|  },
529|  nopeLabelText: {
530|    fontSize: 32,
531|    fontWeight: 'bold',
532|    color: '#FF4444',
533|  },
534|  cardInfo: {
535|    position: 'absolute',
536|    bottom: 0,
537|    left: 0,
538|    right: 0,
539|    padding: 20,
540|    backgroundColor: 'rgba(0,0,0,0.7)',
541|  },
542|  nameRow: {
543|    flexDirection: 'row',
544|    alignItems: 'center',
545|    gap: 8,
546|  },
547|  cardName: {
548|    fontSize: 28,
549|    fontWeight: 'bold',
550|    color: '#FFFFFF',
551|  },
552|  locationRow: {
553|    flexDirection: 'row',
554|    alignItems: 'center',
555|    marginTop: 4,
556|    gap: 4,
557|  },
558|  cardLocation: {
559|    fontSize: 14,
560|    color: '#D4AF37',
561|  },
562|  cardBio: {
563|    fontSize: 14,
564|    color: '#CCCCCC',
565|    marginTop: 8,
566|  },
567|  actions: {
568|    flexDirection: 'row',
569|    justifyContent: 'center',
570|    paddingVertical: 20,
571|    gap: 40,
572|  },
573|  actionButton: {
574|    width: 70,
575|    height: 70,
576|    borderRadius: 35,
577|    justifyContent: 'center',
578|    alignItems: 'center',
579|    shadowColor: '#000',
580|    shadowOffset: { width: 0, height: 2 },
581|    shadowOpacity: 0.3,
582|    shadowRadius: 4,
583|    elevation: 4,
584|  },
585|  passButton: {
586|    backgroundColor: '#1a1a1a',
587|    borderWidth: 2,
588|    borderColor: '#FF4444',
589|  },
590|  likeButton: {
591|    backgroundColor: '#1a1a1a',
592|    borderWidth: 2,
593|    borderColor: '#C41E3A',
594|  },
595|  matchOverlay: {
596|    position: 'absolute',
597|    top: 0,
598|    left: 0,
599|    right: 0,
600|    bottom: 0,
601|    backgroundColor: 'rgba(0,0,0,0.9)',
602|    justifyContent: 'center',
603|    alignItems: 'center',
604|    zIndex: 100,
605|  },
606|  matchContent: {
607|    alignItems: 'center',
608|    padding: 40,
609|  },
610|  matchTitle: {
611|    fontSize: 42,
612|    fontWeight: 'bold',
613|    color: '#D4AF37',
614|    marginBottom: 8,
615|  },
616|  matchSubtitle: {
617|    fontSize: 18,
618|    color: '#FFFFFF',
619|    marginBottom: 24,
620|    textAlign: 'center',
621|  },
622|  matchImage: {
623|    width: 150,
624|    height: 150,
625|    borderRadius: 75,
626|    borderWidth: 3,
627|    borderColor: '#D4AF37',
628|    marginBottom: 24,
629|  },
630|  matchButton: {
631|    backgroundColor: '#C41E3A',
632|    paddingVertical: 16,
633|    paddingHorizontal: 48,
634|    borderRadius: 30,
635|  },
636|  matchButtonText: {
637|    fontSize: 18,
638|    fontWeight: '600',
639|    color: '#FFFFFF',
640|  },
641|});
642|

===END

===FILE: /app/frontend/app/(tabs)/likes.tsx
/app/frontend/app/(tabs)/likes.tsx:
1|import React, { useState, useEffect } from 'react';
2|import {
3|  View,
4|  Text,
5|  StyleSheet,
6|  FlatList,
7|  Image,
8|  TouchableOpacity,
9|  ActivityIndicator,
10|  Alert,
11|} from 'react-native';
12|import { SafeAreaView } from 'react-native-safe-area-context';
13|import { Ionicons } from '@expo/vector-icons';
14|import axios from 'axios';
15|import AsyncStorage from '@react-native-async-storage/async-storage';
16|
17|const BACKEND_URL = process.env.EXPO_PUBLIC_BACKEND_URL;
18|
19|interface LikeData {
20|  user: {
21|    user_id: string;
22|    name: string;
23|    age?: number;
24|    photos: string[];
25|    city?: string;
26|    is_verified: boolean;
27|  };
28|  liked_at: string;
29|}
30|
31|export default function LikesScreen() {
32|  const [likes, setLikes] = useState<LikeData[]>([]);
33|  const [loading, setLoading] = useState(true);
34|  const [refreshing, setRefreshing] = useState(false);
35|
36|  useEffect(() => {
37|    fetchLikes();
38|  }, []);
39|
40|  const fetchLikes = async () => {
41|    try {
42|      const token = await AsyncStorage.getItem('session_token');
43|      const response = await axios.get(`${BACKEND_URL}/api/likes/received`, {
44|        headers: { Authorization: `Bearer ${token}` },
45|      });
46|      setLikes(response.data);
47|    } catch (error) {
48|      console.error('Error fetching likes:', error);
49|    } finally {
50|      setLoading(false);
51|      setRefreshing(false);
52|    }
53|  };
54|
55|  const handleLikeBack = async (userId: string) => {
56|    try {
57|      const token = await AsyncStorage.getItem('session_token');
58|      const response = await axios.post(
59|        `${BACKEND_URL}/api/like`,
60|        { target_user_id: userId },
61|        { headers: { Authorization: `Bearer ${token}` } }
62|      );
63|
64|      if (response.data.is_match) {
65|        Alert.alert('¡Match!', '¡Ahora pueden chatear!', [
66|          { text: 'Genial', onPress: fetchLikes },
67|        ]);
68|      } else {
69|        fetchLikes();
70|      }
71|    } catch (error) {
72|      console.error('Error liking back:', error);
73|    }
74|  };
75|
76|  const renderLikeItem = ({ item }: { item: LikeData }) => (
77|    <View style={styles.likeCard}>
78|      <Image
79|        source={{ uri: item.user.photos[0] }}
80|        style={styles.likeImage}
81|      />
82|      <View style={styles.likeInfo}>
83|        <View style={styles.nameRow}>
84|          <Text style={styles.likeName}>
85|            {item.user.name}
86|            {item.user.age ? `, ${item.user.age}` : ''}
87|          </Text>
88|          {item.user.is_verified && (
89|            <Ionicons name="shield-checkmark" size={18} color="#D4AF37" />
90|          )}
91|        </View>
92|        {item.user.city && (
93|          <Text style={styles.likeCity}>{item.user.city}</Text>
94|        )}
95|      </View>
96|      <TouchableOpacity
97|        style={styles.likeBackButton}
98|        onPress={() => handleLikeBack(item.user.user_id)}
99|      >
100|        <Ionicons name="heart" size={24} color="#FFFFFF" />
101|      </TouchableOpacity>
102|    </View>
103|  );
104|
105|  if (loading) {
106|    return (
107|      <SafeAreaView style={styles.container}>
108|        <View style={styles.loadingContainer}>
109|          <ActivityIndicator size="large" color="#C41E3A" />
110|        </View>
111|      </SafeAreaView>
112|    );
113|  }
114|
115|  return (
116|    <SafeAreaView style={styles.container}>
117|      <View style={styles.header}>
118|        <Text style={styles.headerTitle}>Les Gustas</Text>
119|        <Text style={styles.headerSubtitle}>
120|          {likes.length} {likes.length === 1 ? 'persona' : 'personas'}
121|        </Text>
122|      </View>
123|
124|      {likes.length === 0 ? (
125|        <View style={styles.emptyContainer}>
126|          <Ionicons name="heart-outline" size={80} color="#333333" />
127|          <Text style={styles.emptyTitle}>Aún no tienes likes</Text>
128|          <Text style={styles.emptySubtitle}>
129|            Sigue deslizando para encontrar a alguien especial
130|          </Text>
131|        </View>
132|      ) : (
133|        <FlatList
134|          data={likes}
135|          renderItem={renderLikeItem}
136|          keyExtractor={(item) => item.user.user_id}
137|          contentContainerStyle={styles.listContent}
138|          refreshing={refreshing}
139|          onRefresh={() => {
140|            setRefreshing(true);
141|            fetchLikes();
142|          }}
143|        />
144|      )}
145|    </SafeAreaView>
146|  );
147|}
148|
149|const styles = StyleSheet.create({
150|  container: {
151|    flex: 1,
152|    backgroundColor: '#000000',
153|  },
154|  header: {
155|    paddingHorizontal: 20,
156|    paddingVertical: 16,
157|  },
158|  headerTitle: {
159|    fontSize: 28,
160|    fontWeight: 'bold',
161|    color: '#FFFFFF',
162|  },
163|  headerSubtitle: {
164|    fontSize: 14,
165|    color: '#D4AF37',
166|    marginTop: 4,
167|  },
168|  loadingContainer: {
169|    flex: 1,
170|    justifyContent: 'center',
171|    alignItems: 'center',
172|  },
173|  emptyContainer: {
174|    flex: 1,
175|    justifyContent: 'center',
176|    alignItems: 'center',
177|    paddingHorizontal: 40,
178|  },
179|  emptyTitle: {
180|    fontSize: 24,
181|    fontWeight: 'bold',
182|    color: '#FFFFFF',
183|    marginTop: 20,
184|  },
185|  emptySubtitle: {
186|    fontSize: 16,
187|    color: '#888888',
188|    textAlign: 'center',
189|    marginTop: 8,
190|  },
191|  listContent: {
192|    padding: 16,
193|  },
194|  likeCard: {
195|    flexDirection: 'row',
196|    alignItems: 'center',
197|    backgroundColor: '#1a1a1a',
198|    borderRadius: 16,
199|    padding: 12,
200|    marginBottom: 12,
201|    borderWidth: 1,
202|    borderColor: '#333333',
203|  },
204|  likeImage: {
205|    width: 70,
206|    height: 70,
207|    borderRadius: 35,
208|    borderWidth: 2,
209|    borderColor: '#C41E3A',
210|  },
211|  likeInfo: {
212|    flex: 1,
213|    marginLeft: 16,
214|  },
215|  nameRow: {
216|    flexDirection: 'row',
217|    alignItems: 'center',
218|    gap: 8,
219|  },
220|  likeName: {
221|    fontSize: 18,
222|    fontWeight: '600',
223|    color: '#FFFFFF',
224|  },
225|  likeCity: {
226|    fontSize: 14,
227|    color: '#888888',
228|    marginTop: 4,
229|  },
230|  likeBackButton: {
231|    backgroundColor: '#C41E3A',
232|    width: 50,
233|    height: 50,
234|    borderRadius: 25,
235|    justifyContent: 'center',
236|    alignItems: 'center',
237|  },
238|});
239|

===END

Action: {"type": "mcp_tool", "tool_name": "mcp_view_bulk", "tool_arguments": {"paths": ["/app/frontend/app/(tabs)/matches.tsx", "/app/frontend/app/(tabs)/profile.tsx"]}}
Observation: ===FILE: /app/frontend/app/(tabs)/matches.tsx
/app/frontend/app/(tabs)/matches.tsx:
1|import React, { useState, useEffect } from 'react';
2|import {
3|  View,
4|  Text,
5|  StyleSheet,
6|  FlatList,
7|  Image,
8|  TouchableOpacity,
9|  ActivityIndicator,
10|} from 'react-native';
11|import { SafeAreaView } from 'react-native-safe-area-context';
12|import { useRouter } from 'expo-router';
13|import { Ionicons } from '@expo/vector-icons';
14|import axios from 'axios';
15|import AsyncStorage from '@react-native-async-storage/async-storage';
16|import { format, isToday, isYesterday } from 'date-fns';
17|import { es } from 'date-fns/locale';
18|
19|const BACKEND_URL = process.env.EXPO_PUBLIC_BACKEND_URL;
20|
21|interface MatchData {
22|  match_id: string;
23|  user: {
24|    user_id: string;
25|    name: string;
26|    photos: string[];
27|    is_verified: boolean;
28|  };
29|  last_message?: {
30|    content: string;
31|    sender_id: string;
32|    timestamp: string;
33|  };
34|  unread_count: number;
35|  created_at: string;
36|}
37|
38|export default function MatchesScreen() {
39|  const router = useRouter();
40|  const [matches, setMatches] = useState<MatchData[]>([]);
41|  const [loading, setLoading] = useState(true);
42|  const [refreshing, setRefreshing] = useState(false);
43|
44|  useEffect(() => {
45|    fetchMatches();
46|  }, []);
47|
48|  const fetchMatches = async () => {
49|    try {
50|      const token = await AsyncStorage.getItem('session_token');
51|      const response = await axios.get(`${BACKEND_URL}/api/matches`, {
52|        headers: { Authorization: `Bearer ${token}` },
53|      });
54|      setMatches(response.data);
55|    } catch (error) {
56|      console.error('Error fetching matches:', error);
57|    } finally {
58|      setLoading(false);
59|      setRefreshing(false);
60|    }
61|  };
62|
63|  const formatMessageTime = (timestamp: string) => {
64|    const date = new Date(timestamp);
65|    if (isToday(date)) {
66|      return format(date, 'HH:mm');
67|    } else if (isYesterday(date)) {
68|      return 'Ayer';
69|    }
70|    return format(date, 'dd/MM', { locale: es });
71|  };
72|
73|  const renderMatchItem = ({ item }: { item: MatchData }) => (
74|    <TouchableOpacity
75|      style={styles.matchCard}
76|      onPress={() => router.push(`/chat/${item.match_id}`)}
77|    >
78|      <View style={styles.avatarContainer}>
79|        <Image
80|          source={{ uri: item.user.photos[0] }}
81|          style={styles.matchImage}
82|        />
83|        {item.unread_count > 0 && (
84|          <View style={styles.unreadBadge}>
85|            <Text style={styles.unreadText}>{item.unread_count}</Text>
86|          </View>
87|        )}
88|      </View>
89|      <View style={styles.matchInfo}>
90|        <View style={styles.nameRow}>
91|          <Text style={styles.matchName}>{item.user.name}</Text>
92|          {item.user.is_verified && (
93|            <Ionicons name="shield-checkmark" size={16} color="#D4AF37" />
94|          )}
95|        </View>
96|        {item.last_message ? (
97|          <Text style={styles.lastMessage} numberOfLines={1}>
98|            {item.last_message.content}
99|          </Text>
100|        ) : (
101|          <Text style={styles.newMatchText}>¡Nuevo match! Di hola</Text>
102|        )}
103|      </View>
104|      {item.last_message && (
105|        <Text style={styles.messageTime}>
106|          {formatMessageTime(item.last_message.timestamp)}
107|        </Text>
108|      )}
109|    </TouchableOpacity>
110|  );
111|
112|  if (loading) {
113|    return (
114|      <SafeAreaView style={styles.container}>
115|        <View style={styles.loadingContainer}>
116|          <ActivityIndicator size="large" color="#C41E3A" />
117|        </View>
118|      </SafeAreaView>
119|    );
120|  }
121|
122|  return (
123|    <SafeAreaView style={styles.container}>
124|      <View style={styles.header}>
125|        <Text style={styles.headerTitle}>Matches</Text>
126|        <Text style={styles.headerSubtitle}>
127|          {matches.length} {matches.length === 1 ? 'conexión' : 'conexiones'}
128|        </Text>
129|      </View>
130|
131|      {matches.length === 0 ? (
132|        <View style={styles.emptyContainer}>
133|          <Ionicons name="chatbubbles-outline" size={80} color="#333333" />
134|          <Text style={styles.emptyTitle}>Sin matches aún</Text>
135|          <Text style={styles.emptySubtitle}>
136|            Cuando hagan match mutuamente, aparecerán aquí
137|          </Text>
138|        </View>
139|      ) : (
140|        <FlatList
141|          data={matches}
142|          renderItem={renderMatchItem}
143|          keyExtractor={(item) => item.match_id}
144|          contentContainerStyle={styles.listContent}
145|          refreshing={refreshing}
146|          onRefresh={() => {
147|            setRefreshing(true);
148|            fetchMatches();
149|          }}
150|        />
151|      )}
152|    </SafeAreaView>
153|  );
154|}
155|
156|const styles = StyleSheet.create({
157|  container: {
158|    flex: 1,
159|    backgroundColor: '#000000',
160|  },
161|  header: {
162|    paddingHorizontal: 20,
163|    paddingVertical: 16,
164|  },
165|  headerTitle: {
166|    fontSize: 28,
167|    fontWeight: 'bold',
168|    color: '#FFFFFF',
169|  },
170|  headerSubtitle: {
171|    fontSize: 14,
172|    color: '#D4AF37',
173|    marginTop: 4,
174|  },
175|  loadingContainer: {
176|    flex: 1,
177|    justifyContent: 'center',
178|    alignItems: 'center',
179|  },
180|  emptyContainer: {
181|    flex: 1,
182|    justifyContent: 'center',
183|    alignItems: 'center',
184|    paddingHorizontal: 40,
185|  },
186|  emptyTitle: {
187|    fontSize: 24,
188|    fontWeight: 'bold',
189|    color: '#FFFFFF',
190|    marginTop: 20,
191|  },
192|  emptySubtitle: {
193|    fontSize: 16,
194|    color: '#888888',
195|    textAlign: 'center',
196|    marginTop: 8,
197|  },
198|  listContent: {
199|    padding: 16,
200|  },
201|  matchCard: {
202|    flexDirection: 'row',
203|    alignItems: 'center',
204|    backgroundColor: '#1a1a1a',
205|    borderRadius: 16,
206|    padding: 12,
207|    marginBottom: 12,
208|    borderWidth: 1,
209|    borderColor: '#333333',
210|  },
211|  avatarContainer: {
212|    position: 'relative',
213|  },
214|  matchImage: {
215|    width: 60,
216|    height: 60,
217|    borderRadius: 30,
218|    borderWidth: 2,
219|    borderColor: '#D4AF37',
220|  },
221|  unreadBadge: {
222|    position: 'absolute',
223|    top: -4,
224|    right: -4,
225|    backgroundColor: '#C41E3A',
226|    borderRadius: 12,
227|    minWidth: 24,
228|    height: 24,
229|    justifyContent: 'center',
230|    alignItems: 'center',
231|    paddingHorizontal: 6,
232|  },
233|  unreadText: {
234|    color: '#FFFFFF',
235|    fontSize: 12,
236|    fontWeight: 'bold',
237|  },
238|  matchInfo: {
239|    flex: 1,
240|    marginLeft: 16,
241|  },
242|  nameRow: {
243|    flexDirection: 'row',
244|    alignItems: 'center',
245|    gap: 6,
246|  },
247|  matchName: {
248|    fontSize: 18,
249|    fontWeight: '600',
250|    color: '#FFFFFF',
251|  },
252|  lastMessage: {
253|    fontSize: 14,
254|    color: '#888888',
255|    marginTop: 4,
256|  },
257|  newMatchText: {
258|    fontSize: 14,
259|    color: '#D4AF37',
260|    marginTop: 4,
261|    fontStyle: 'italic',
262|  },
263|  messageTime: {
264|    fontSize: 12,
265|    color: '#666666',
266|  },
267|});
268|

===END

===FILE: /app/frontend/app/(tabs)/profile.tsx
/app/frontend/app/(tabs)/profile.tsx:
1|import React from 'react';
2|import {
3|  View,
4|  Text,
5|  StyleSheet,
6|  Image,
7|  TouchableOpacity,
8|  ScrollView,
9|  Alert,
10|} from 'react-native';
11|import { SafeAreaView } from 'react-native-safe-area-context';
12|import { useRouter } from 'expo-router';
13|import { Ionicons } from '@expo/vector-icons';
14|import { useAuth } from '../_layout';
15|
16|export default function ProfileScreen() {
17|  const router = useRouter();
18|  const { user, logout } = useAuth();
19|
20|  const handleLogout = () => {
21|    Alert.alert(
22|      'Cerrar sesión',
23|      '¿Estás seguro de que quieres cerrar sesión?',
24|      [
25|        { text: 'Cancelar', style: 'cancel' },
26|        { text: 'Cerrar sesión', onPress: logout, style: 'destructive' },
27|      ]
28|    );
29|  };
30|
31|  const profilePhoto = user?.photos?.[0] || user?.picture;
32|
33|  return (
34|    <SafeAreaView style={styles.container}>
35|      <ScrollView contentContainerStyle={styles.scrollContent}>
36|        {/* Header */}
37|        <View style={styles.header}>
38|          <Text style={styles.headerTitle}>Mi Perfil</Text>
39|        </View>
40|
41|        {/* Profile Card */}
42|        <View style={styles.profileCard}>
43|          <View style={styles.photoContainer}>
44|            {profilePhoto ? (
45|              <Image source={{ uri: profilePhoto }} style={styles.profilePhoto} />
46|            ) : (
47|              <View style={styles.placeholderPhoto}>
48|                <Ionicons name="person" size={60} color="#666666" />
49|              </View>
50|            )}
51|            {user?.is_verified && (
52|              <View style={styles.verifiedBadge}>
53|                <Ionicons name="shield-checkmark" size={24} color="#D4AF37" />
54|              </View>
55|            )}
56|          </View>
57|
58|          <Text style={styles.userName}>
59|            {user?.name}
60|            {user?.age ? `, ${user.age}` : ''}
61|          </Text>
62|          
63|          {user?.city && (
64|            <View style={styles.locationRow}>
65|              <Ionicons name="location" size={16} color="#D4AF37" />
66|              <Text style={styles.locationText}>{user.city}</Text>
67|            </View>
68|          )}
69|
70|          {user?.bio && (
71|            <Text style={styles.bio}>{user.bio}</Text>
72|          )}
73|
74|          <TouchableOpacity
75|            style={styles.editButton}
76|            onPress={() => router.push('/profile/edit')}
77|          >
78|            <Ionicons name="pencil" size={20} color="#FFFFFF" />
79|            <Text style={styles.editButtonText}>Editar perfil</Text>
80|          </TouchableOpacity>
81|        </View>
82|
83|        {/* Photos Grid */}
84|        {user?.photos && user.photos.length > 0 && (
85|          <View style={styles.section}>
86|            <Text style={styles.sectionTitle}>Mis fotos</Text>
87|            <View style={styles.photosGrid}>
88|              {user.photos.map((photo, index) => (
89|                <Image
90|                  key={index}
91|                  source={{ uri: photo }}
92|                  style={styles.gridPhoto}
93|                />
94|              ))}
95|            </View>
96|          </View>
97|        )}
98|
99|        {/* Settings */}
100|        <View style={styles.section}>
101|          <Text style={styles.sectionTitle}>Configuración</Text>
102|          
103|          <TouchableOpacity style={styles.settingItem}>
104|            <Ionicons name="notifications" size={24} color="#D4AF37" />
105|            <Text style={styles.settingText}>Notificaciones</Text>
106|            <Ionicons name="chevron-forward" size={20} color="#666666" />
107|          </TouchableOpacity>
108|
109|          <TouchableOpacity style={styles.settingItem}>
110|            <Ionicons name="shield" size={24} color="#D4AF37" />
111|            <Text style={styles.settingText}>Privacidad</Text>
112|            <Ionicons name="chevron-forward" size={20} color="#666666" />
113|          </TouchableOpacity>
114|
115|          <TouchableOpacity style={styles.settingItem}>
116|            <Ionicons name="help-circle" size={24} color="#D4AF37" />
117|            <Text style={styles.settingText}>Ayuda</Text>
118|            <Ionicons name="chevron-forward" size={20} color="#666666" />
119|          </TouchableOpacity>
120|
121|          <TouchableOpacity
122|            style={[styles.settingItem, styles.logoutItem]}
123|            onPress={handleLogout}
124|          >
125|            <Ionicons name="log-out" size={24} color="#C41E3A" />
126|            <Text style={[styles.settingText, styles.logoutText]}>
127|              Cerrar sesión
128|            </Text>
129|          </TouchableOpacity>
130|        </View>
131|
132|        {/* Verification Status */}
133|        {!user?.is_verified && (
134|          <TouchableOpacity
135|            style={styles.verifyBanner}
136|            onPress={() => router.push('/profile/edit')}
137|          >
138|            <Ionicons name="shield-outline" size={24} color="#D4AF37" />
139|            <View style={styles.verifyBannerContent}>
140|              <Text style={styles.verifyBannerTitle}>Verifica tu perfil</Text>
141|              <Text style={styles.verifyBannerText}>
142|                Obtén la insignia de verificación
143|              </Text>
144|            </View>
145|            <Ionicons name="chevron-forward" size={20} color="#D4AF37" />
146|          </TouchableOpacity>
147|        )}
148|      </ScrollView>
149|    </SafeAreaView>
150|  );
151|}
152|
153|const styles = StyleSheet.create({
154|  container: {
155|    flex: 1,
156|    backgroundColor: '#000000',
157|  },
158|  scrollContent: {
159|    paddingBottom: 40,
160|  },
161|  header: {
162|    paddingHorizontal: 20,
163|    paddingVertical: 16,
164|  },
165|  headerTitle: {
166|    fontSize: 28,
167|    fontWeight: 'bold',
168|    color: '#FFFFFF',
169|  },
170|  profileCard: {
171|    alignItems: 'center',
172|    padding: 24,
173|    marginHorizontal: 16,
174|    backgroundColor: '#1a1a1a',
175|    borderRadius: 20,
176|    borderWidth: 1,
177|    borderColor: '#333333',
178|  },
179|  photoContainer: {
180|    position: 'relative',
181|    marginBottom: 16,
182|  },
183|  profilePhoto: {
184|    width: 120,
185|    height: 120,
186|    borderRadius: 60,
187|    borderWidth: 3,
188|    borderColor: '#D4AF37',
189|  },
190|  placeholderPhoto: {
191|    width: 120,
192|    height: 120,
193|    borderRadius: 60,
194|    backgroundColor: '#333333',
195|    justifyContent: 'center',
196|    alignItems: 'center',
197|    borderWidth: 3,
198|    borderColor: '#D4AF37',
199|  },
200|  verifiedBadge: {
201|    position: 'absolute',
202|    bottom: 0,
203|    right: 0,
204|    backgroundColor: '#000000',
205|    borderRadius: 15,
206|    padding: 4,
207|  },
208|  userName: {
209|    fontSize: 28,
210|    fontWeight: 'bold',
211|    color: '#FFFFFF',
212|  },
213|  locationRow: {
214|    flexDirection: 'row',
215|    alignItems: 'center',
216|    marginTop: 8,
217|    gap: 4,
218|  },
219|  locationText: {
220|    fontSize: 16,
221|    color: '#D4AF37',
222|  },
223|  bio: {
224|    fontSize: 16,
225|    color: '#CCCCCC',
226|    textAlign: 'center',
227|    marginTop: 12,
228|    paddingHorizontal: 20,
229|  },
230|  editButton: {
231|    flexDirection: 'row',
232|    alignItems: 'center',
233|    backgroundColor: '#C41E3A',
234|    paddingVertical: 12,
235|    paddingHorizontal: 24,
236|    borderRadius: 25,
237|    marginTop: 20,
238|    gap: 8,
239|  },
240|  editButtonText: {
241|    fontSize: 16,
242|    fontWeight: '600',
243|    color: '#FFFFFF',
244|  },
245|  section: {
246|    marginTop: 24,
247|    paddingHorizontal: 16,
248|  },
249|  sectionTitle: {
250|    fontSize: 18,
251|    fontWeight: '600',
252|    color: '#FFFFFF',
253|    marginBottom: 16,
254|  },
255|  photosGrid: {
256|    flexDirection: 'row',
257|    flexWrap: 'wrap',
258|    gap: 8,
259|  },
260|  gridPhoto: {
261|    width: '31%',
262|    aspectRatio: 1,
263|    borderRadius: 12,
264|  },
265|  settingItem: {
266|    flexDirection: 'row',
267|    alignItems: 'center',
268|    backgroundColor: '#1a1a1a',
269|    padding: 16,
270|    borderRadius: 12,
271|    marginBottom: 8,
272|    gap: 16,
273|  },
274|  settingText: {
275|    flex: 1,
276|    fontSize: 16,
277|    color: '#FFFFFF',
278|  },
279|  logoutItem: {
280|    marginTop: 8,
281|  },
282|  logoutText: {
283|    color: '#C41E3A',
284|  },
285|  verifyBanner: {
286|    flexDirection: 'row',
287|    alignItems: 'center',
288|    backgroundColor: '#1a1a0a',
289|    padding: 16,
290|    marginHorizontal: 16,
291|    marginTop: 24,
292|    borderRadius: 12,
293|    borderWidth: 1,
294|    borderColor: '#D4AF37',
295|    gap: 12,
296|  },
297|  verifyBannerContent: {
298|    flex: 1,
299|  },
300|  verifyBannerTitle: {
301|    fontSize: 16,
302|    fontWeight: '600',
303|    color: '#D4AF37',
304|  },
305|  verifyBannerText: {
306|    fontSize: 14,
307|    color: '#888888',
308|    marginTop: 2,
309|  },
310|});
311|

===END

Action: {"type": "mcp_tool", "tool_name": "mcp_view_bulk", "tool_arguments": {"paths": ["/app/frontend/app/chat/[matchId].tsx", "/app/frontend/app/profile/edit.tsx"]}}
Observation: ===FILE: /app/frontend/app/chat/[matchId].tsx
/app/frontend/app/chat/[matchId].tsx:
1|import React, { useState, useEffect, useRef } from 'react';
2|import {
3|  View,
4|  Text,
5|  StyleSheet,
6|  TextInput,
7|  TouchableOpacity,
8|  FlatList,
9|  Image,
10|  KeyboardAvoidingView,
11|  Platform,
12|  ActivityIndicator,
13|} from 'react-native';
14|import { SafeAreaView } from 'react-native-safe-area-context';
15|import { useRouter, useLocalSearchParams } from 'expo-router';
16|import { Ionicons } from '@expo/vector-icons';
17|import axios from 'axios';
18|import AsyncStorage from '@react-native-async-storage/async-storage';
19|import { format, isToday, isYesterday } from 'date-fns';
20|import { es } from 'date-fns/locale';
21|import { useAuth } from '../_layout';
22|
23|const BACKEND_URL = process.env.EXPO_PUBLIC_BACKEND_URL;
24|
25|interface MessageData {
26|  id: string;
27|  match_id: string;
28|  sender_id: string;
29|  content: string;
30|  timestamp: string;
31|  read: boolean;
32|}
33|
34|interface OtherUser {
35|  user_id: string;
36|  name: string;
37|  photos: string[];
38|  is_verified: boolean;
39|}
40|
41|export default function ChatScreen() {
42|  const router = useRouter();
43|  const { matchId } = useLocalSearchParams<{ matchId: string }>();
44|  const { user } = useAuth();
45|  const [messages, setMessages] = useState<MessageData[]>([]);
46|  const [otherUser, setOtherUser] = useState<OtherUser | null>(null);
47|  const [newMessage, setNewMessage] = useState('');
48|  const [loading, setLoading] = useState(true);
49|  const [sending, setSending] = useState(false);
50|  const flatListRef = useRef<FlatList>(null);
51|
52|  useEffect(() => {
53|    fetchMessages();
54|    const interval = setInterval(fetchMessages, 5000); // Poll every 5 seconds
55|    return () => clearInterval(interval);
56|  }, [matchId]);
57|
58|  const fetchMessages = async () => {
59|    try {
60|      const token = await AsyncStorage.getItem('session_token');
61|      const response = await axios.get(`${BACKEND_URL}/api/chat/${matchId}`, {
62|        headers: { Authorization: `Bearer ${token}` },
63|      });
64|      setMessages(response.data.messages);
65|      setOtherUser(response.data.other_user);
66|    } catch (error) {
67|      console.error('Error fetching messages:', error);
68|    } finally {
69|      setLoading(false);
70|    }
71|  };
72|
73|  const sendMessage = async () => {
74|    if (!newMessage.trim() || sending) return;
75|
76|    setSending(true);
77|    try {
78|      const token = await AsyncStorage.getItem('session_token');
79|      const response = await axios.post(
80|        `${BACKEND_URL}/api/chat/${matchId}`,
81|        { content: newMessage.trim() },
82|        { headers: { Authorization: `Bearer ${token}` } }
83|      );
84|
85|      setMessages((prev) => [...prev, response.data]);
86|      setNewMessage('');
87|      setTimeout(() => flatListRef.current?.scrollToEnd(), 100);
88|    } catch (error) {
89|      console.error('Error sending message:', error);
90|    } finally {
91|      setSending(false);
92|    }
93|  };
94|
95|  const formatMessageTime = (timestamp: string) => {
96|    const date = new Date(timestamp);
97|    if (isToday(date)) {
98|      return format(date, 'HH:mm');
99|    } else if (isYesterday(date)) {
100|      return 'Ayer ' + format(date, 'HH:mm');
101|    }
102|    return format(date, 'dd MMM HH:mm', { locale: es });
103|  };
104|
105|  const renderMessage = ({ item, index }: { item: MessageData; index: number }) => {
106|    const isMe = item.sender_id === user?.user_id;
107|    const showAvatar = !isMe && 
108|      (index === 0 || messages[index - 1].sender_id !== item.sender_id);
109|
110|    return (
111|      <View style={[styles.messageRow, isMe && styles.messageRowMe]}>
112|        {!isMe && showAvatar && otherUser && (
113|          <Image
114|            source={{ uri: otherUser.photos[0] }}
115|            style={styles.messageAvatar}
116|          />
117|        )}
118|        {!isMe && !showAvatar && <View style={styles.avatarPlaceholder} />}
119|        <View
120|          style={[
121|            styles.messageBubble,
122|            isMe ? styles.messageBubbleMe : styles.messageBubbleThem,
123|          ]}
124|        >
125|          <Text style={[styles.messageText, isMe && styles.messageTextMe]}>
126|            {item.content}
127|          </Text>
128|          <Text style={[styles.messageTime, isMe && styles.messageTimeMe]}>
129|            {formatMessageTime(item.timestamp)}
130|          </Text>
131|        </View>
132|      </View>
133|    );
134|  };
135|
136|  if (loading) {
137|    return (
138|      <SafeAreaView style={styles.container}>
139|        <View style={styles.loadingContainer}>
140|          <ActivityIndicator size="large" color="#C41E3A" />
141|        </View>
142|      </SafeAreaView>
143|    );
144|  }
145|
146|  return (
147|    <SafeAreaView style={styles.container} edges={['top']}>
148|      {/* Header */}
149|      <View style={styles.header}>
150|        <TouchableOpacity
151|          style={styles.backButton}
152|          onPress={() => router.back()}
153|        >
154|          <Ionicons name="chevron-back" size={28} color="#FFFFFF" />
155|        </TouchableOpacity>
156|        {otherUser && (
157|          <View style={styles.headerUser}>
158|            <Image
159|              source={{ uri: otherUser.photos[0] }}
160|              style={styles.headerAvatar}
161|            />
162|            <View>
163|              <View style={styles.headerNameRow}>
164|                <Text style={styles.headerName}>{otherUser.name}</Text>
165|                {otherUser.is_verified && (
166|                  <Ionicons name="shield-checkmark" size={16} color="#D4AF37" />
167|                )}
168|              </View>
169|              <Text style={styles.headerStatus}>En línea</Text>
170|            </View>
171|          </View>
172|        )}
173|      </View>
174|
175|      {/* Messages */}
176|      <KeyboardAvoidingView
177|        style={styles.chatContainer}
178|        behavior={Platform.OS === 'ios' ? 'padding' : 'height'}
179|        keyboardVerticalOffset={0}
180|      >
181|        <FlatList
182|          ref={flatListRef}
183|          data={messages}
184|          renderItem={renderMessage}
185|          keyExtractor={(item) => item.id}
186|          contentContainerStyle={styles.messagesList}
187|          onContentSizeChange={() => flatListRef.current?.scrollToEnd()}
188|          ListEmptyComponent={
189|            <View style={styles.emptyChat}>
190|              <Ionicons name="chatbubbles-outline" size={60} color="#333333" />
191|              <Text style={styles.emptyChatText}>
192|                ¡Di hola a {otherUser?.name}!
193|              </Text>
194|            </View>
195|          }
196|        />
197|
198|        {/* Input */}
199|        <View style={styles.inputContainer}>
200|          <TextInput
201|            style={styles.input}
202|            placeholder="Escribe un mensaje..."
203|            placeholderTextColor="#666666"
204|            value={newMessage}
205|            onChangeText={setNewMessage}
206|            multiline
207|            maxLength={500}
208|          />
209|          <TouchableOpacity
210|            style={[
211|              styles.sendButton,
212|              (!newMessage.trim() || sending) && styles.sendButtonDisabled,
213|            ]}
214|            onPress={sendMessage}
215|            disabled={!newMessage.trim() || sending}
216|          >
217|            {sending ? (
218|              <ActivityIndicator size="small" color="#FFFFFF" />
219|            ) : (
220|              <Ionicons name="send" size={20} color="#FFFFFF" />
221|            )}
222|          </TouchableOpacity>
223|        </View>
224|      </KeyboardAvoidingView>
225|    </SafeAreaView>
226|  );
227|}
228|
229|const styles = StyleSheet.create({
230|  container: {
231|    flex: 1,
232|    backgroundColor: '#000000',
233|  },
234|  loadingContainer: {
235|    flex: 1,
236|    justifyContent: 'center',
237|    alignItems: 'center',
238|  },
239|  header: {
240|    flexDirection: 'row',
241|    alignItems: 'center',
242|    padding: 16,
243|    borderBottomWidth: 1,
244|    borderBottomColor: '#333333',
245|  },
246|  backButton: {
247|    marginRight: 12,
248|  },
249|  headerUser: {
250|    flexDirection: 'row',
251|    alignItems: 'center',
252|    flex: 1,
253|  },
254|  headerAvatar: {
255|    width: 44,
256|    height: 44,
257|    borderRadius: 22,
258|    marginRight: 12,
259|    borderWidth: 2,
260|    borderColor: '#D4AF37',
261|  },
262|  headerNameRow: {
263|    flexDirection: 'row',
264|    alignItems: 'center',
265|    gap: 6,
266|  },
267|  headerName: {
268|    fontSize: 18,
269|    fontWeight: '600',
270|    color: '#FFFFFF',
271|  },
272|  headerStatus: {
273|    fontSize: 12,
274|    color: '#4CAF50',
275|    marginTop: 2,
276|  },
277|  chatContainer: {
278|    flex: 1,
279|  },
280|  messagesList: {
281|    padding: 16,
282|    flexGrow: 1,
283|  },
284|  emptyChat: {
285|    flex: 1,
286|    justifyContent: 'center',
287|    alignItems: 'center',
288|    paddingTop: 100,
289|  },
290|  emptyChatText: {
291|    fontSize: 16,
292|    color: '#666666',
293|    marginTop: 16,
294|  },
295|  messageRow: {
296|    flexDirection: 'row',
297|    marginBottom: 8,
298|    alignItems: 'flex-end',
299|  },
300|  messageRowMe: {
301|    justifyContent: 'flex-end',
302|  },
303|  messageAvatar: {
304|    width: 32,
305|    height: 32,
306|    borderRadius: 16,
307|    marginRight: 8,
308|  },
309|  avatarPlaceholder: {
310|    width: 32,
311|    marginRight: 8,
312|  },
313|  messageBubble: {
314|    maxWidth: '75%',
315|    padding: 12,
316|    borderRadius: 18,
317|  },
318|  messageBubbleThem: {
319|    backgroundColor: '#1a1a1a',
320|    borderBottomLeftRadius: 4,
321|  },
322|  messageBubbleMe: {
323|    backgroundColor: '#C41E3A',
324|    borderBottomRightRadius: 4,
325|  },
326|  messageText: {
327|    fontSize: 16,
328|    color: '#FFFFFF',
329|  },
330|  messageTextMe: {
331|    color: '#FFFFFF',
332|  },
333|  messageTime: {
334|    fontSize: 10,
335|    color: '#888888',
336|    marginTop: 4,
337|    alignSelf: 'flex-end',
338|  },
339|  messageTimeMe: {
340|    color: 'rgba(255,255,255,0.7)',
341|  },
342|  inputContainer: {
343|    flexDirection: 'row',
344|    alignItems: 'flex-end',
345|    padding: 12,
346|    borderTopWidth: 1,
347|    borderTopColor: '#333333',
348|    backgroundColor: '#0a0a0a',
349|  },
350|  input: {
351|    flex: 1,
352|    backgroundColor: '#1a1a1a',
353|    borderRadius: 24,
354|    paddingHorizontal: 16,
355|    paddingVertical: 12,
356|    fontSize: 16,
357|    color: '#FFFFFF',
358|    maxHeight: 100,
359|    marginRight: 8,
360|  },
361|  sendButton: {
362|    width: 48,
363|    height: 48,
364|    borderRadius: 24,
365|    backgroundColor: '#C41E3A',
366|    justifyContent: 'center',
367|    alignItems: 'center',
368|  },
369|  sendButtonDisabled: {
370|    backgroundColor: '#333333',
371|  },
372|});
373|

===END

===FILE: /app/frontend/app/profile/edit.tsx
/app/frontend/app/profile/edit.tsx:
1|import React, { useState, useEffect } from 'react';
2|import {
3|  View,
4|  Text,
5|  StyleSheet,
6|  TextInput,
7|  TouchableOpacity,
8|  ScrollView,
9|  Image,
10|  Alert,
11|  ActivityIndicator,
12|  KeyboardAvoidingView,
13|  Platform,
14|} from 'react-native';
15|import { SafeAreaView } from 'react-native-safe-area-context';
16|import { useRouter } from 'expo-router';
17|import { Ionicons } from '@expo/vector-icons';
18|import * as ImagePicker from 'expo-image-picker';
19|import * as Location from 'expo-location';
20|import axios from 'axios';
21|import AsyncStorage from '@react-native-async-storage/async-storage';
22|import { useAuth } from '../_layout';
23|
24|const BACKEND_URL = process.env.EXPO_PUBLIC_BACKEND_URL;
25|
26|export default function EditProfileScreen() {
27|  const router = useRouter();
28|  const { user, refreshUser } = useAuth();
29|  const [loading, setLoading] = useState(false);
30|  const [name, setName] = useState(user?.name || '');
31|  const [bio, setBio] = useState(user?.bio || '');
32|  const [age, setAge] = useState(user?.age?.toString() || '');
33|  const [gender, setGender] = useState(user?.gender || '');
34|  const [lookingFor, setLookingFor] = useState(user?.looking_for || '');
35|  const [city, setCity] = useState(user?.city || '');
36|  const [photos, setPhotos] = useState<string[]>(user?.photos || []);
37|  const [locationLoading, setLocationLoading] = useState(false);
38|
39|  const genderOptions = [
40|    { value: 'hombre', label: 'Hombre' },
41|    { value: 'mujer', label: 'Mujer' },
42|    { value: 'otro', label: 'Otro' },
43|  ];
44|
45|  const lookingForOptions = [
46|    { value: 'hombre', label: 'Hombres' },
47|    { value: 'mujer', label: 'Mujeres' },
48|    { value: 'todos', label: 'Todos' },
49|  ];
50|
51|  const pickImage = async () => {
52|    if (photos.length >= 6) {
53|      Alert.alert('Límite alcanzado', 'Máximo 6 fotos permitidas');
54|      return;
55|    }
56|
57|    const { status } = await ImagePicker.requestMediaLibraryPermissionsAsync();
58|    if (status !== 'granted') {
59|      Alert.alert('Permiso denegado', 'Necesitamos acceso a tu galería');
60|      return;
61|    }
62|
63|    const result = await ImagePicker.launchImageLibraryAsync({
64|      mediaTypes: ImagePicker.MediaTypeOptions.Images,
65|      allowsEditing: true,
66|      aspect: [3, 4],
67|      quality: 0.8,
68|      base64: true,
69|    });
70|
71|    if (!result.canceled && result.assets[0].base64) {
72|      const base64Image = `data:image/jpeg;base64,${result.assets[0].base64}`;
73|      setPhotos([...photos, base64Image]);
74|    }
75|  };
76|
77|  const takePhoto = async () => {
78|    if (photos.length >= 6) {
79|      Alert.alert('Límite alcanzado', 'Máximo 6 fotos permitidas');
80|      return;
81|    }
82|
83|    const { status } = await ImagePicker.requestCameraPermissionsAsync();
84|    if (status !== 'granted') {
85|      Alert.alert('Permiso denegado', 'Necesitamos acceso a tu cámara');
86|      return;
87|    }
88|
89|    const result = await ImagePicker.launchCameraAsync({
90|      allowsEditing: true,
91|      aspect: [3, 4],
92|      quality: 0.8,
93|      base64: true,
94|    });
95|
96|    if (!result.canceled && result.assets[0].base64) {
97|      const base64Image = `data:image/jpeg;base64,${result.assets[0].base64}`;
98|      setPhotos([...photos, base64Image]);
99|    }
100|  };
101|
102|  const removePhoto = (index: number) => {
103|    setPhotos(photos.filter((_, i) => i !== index));
104|  };
105|
106|  const updateLocation = async () => {
107|    setLocationLoading(true);
108|    try {
109|      const { status } = await Location.requestForegroundPermissionsAsync();
110|      if (status !== 'granted') {
111|        Alert.alert('Permiso denegado', 'Necesitamos acceso a tu ubicación');
112|        return;
113|      }
114|
115|      const location = await Location.getCurrentPositionAsync({});
116|      const [address] = await Location.reverseGeocodeAsync({
117|        latitude: location.coords.latitude,
118|        longitude: location.coords.longitude,
119|      });
120|
121|      const cityName = address.city || address.region || 'Ubicación desconocida';
122|      setCity(cityName);
123|
124|      const token = await AsyncStorage.getItem('session_token');
125|      await axios.put(
126|        `${BACKEND_URL}/api/profile/location`,
127|        {
128|          latitude: location.coords.latitude,
129|          longitude: location.coords.longitude,
130|          city: cityName,
131|        },
132|        { headers: { Authorization: `Bearer ${token}` } }
133|      );
134|
135|      Alert.alert('Éxito', 'Ubicación actualizada');
136|    } catch (error) {
137|      console.error('Error updating location:', error);
138|      Alert.alert('Error', 'No se pudo obtener la ubicación');
139|    } finally {
140|      setLocationLoading(false);
141|    }
142|  };
143|
144|  const requestVerification = async () => {
145|    const { status } = await ImagePicker.requestCameraPermissionsAsync();
146|    if (status !== 'granted') {
147|      Alert.alert('Permiso denegado', 'Necesitamos acceso a tu cámara');
148|      return;
149|    }
150|
151|    Alert.alert(
152|      'Verificación de foto',
153|      'Tómate una selfie para verificar tu identidad',
154|      [
155|        { text: 'Cancelar', style: 'cancel' },
156|        {
157|          text: 'Tomar foto',
158|          onPress: async () => {
159|            const result = await ImagePicker.launchCameraAsync({
160|              allowsEditing: true,
161|              aspect: [1, 1],
162|              quality: 0.8,
163|              base64: true,
164|            });
165|
166|            if (!result.canceled && result.assets[0].base64) {
167|              const base64Image = `data:image/jpeg;base64,${result.assets[0].base64}`;
168|              try {
169|                const token = await AsyncStorage.getItem('session_token');
170|                await axios.post(
171|                  `${BACKEND_URL}/api/profile/verify`,
172|                  { photo: base64Image },
173|                  { headers: { Authorization: `Bearer ${token}` } }
174|                );
175|                Alert.alert('Éxito', '¡Tu perfil ha sido verificado!');
176|                refreshUser();
177|              } catch (error) {
178|                Alert.alert('Error', 'No se pudo verificar');
179|              }
180|            }
181|          },
182|        },
183|      ]
184|    );
185|  };
186|
187|  const saveProfile = async () => {
188|    if (!name.trim()) {
189|      Alert.alert('Error', 'El nombre es requerido');
190|      return;
191|    }
192|
193|    if (!age || parseInt(age) < 18) {
194|      Alert.alert('Error', 'Debes ser mayor de 18 años');
195|      return;
196|    }
197|
198|    if (!gender) {
199|      Alert.alert('Error', 'Selecciona tu género');
200|      return;
201|    }
202|
203|    if (photos.length === 0) {
204|      Alert.alert('Error', 'Agrega al menos una foto');
205|      return;
206|    }
207|
208|    setLoading(true);
209|    try {
210|      const token = await AsyncStorage.getItem('session_token');
211|      await axios.put(
212|        `${BACKEND_URL}/api/profile`,
213|        {
214|          name: name.trim(),
215|          bio: bio.trim(),
216|          age: parseInt(age),
217|          gender,
218|          looking_for: lookingFor,
219|          photos,
220|          city,
221|        },
222|        { headers: { Authorization: `Bearer ${token}` } }
223|      );
224|
225|      await refreshUser();
226|      Alert.alert('Éxito', 'Perfil actualizado', [
227|        { text: 'OK', onPress: () => router.replace('/(tabs)/discover') },
228|      ]);
229|    } catch (error) {
230|      console.error('Error saving profile:', error);
231|      Alert.alert('Error', 'No se pudo guardar el perfil');
232|    } finally {
233|      setLoading(false);
234|    }
235|  };
236|
237|  return (
238|    <SafeAreaView style={styles.container}>
239|      <KeyboardAvoidingView
240|        style={{ flex: 1 }}
241|        behavior={Platform.OS === 'ios' ? 'padding' : undefined}
242|      >
243|        <ScrollView contentContainerStyle={styles.scrollContent}>
244|          {/* Header */}
245|          <View style={styles.header}>
246|            <TouchableOpacity
247|              onPress={() => router.back()}
248|              style={styles.backButton}
249|            >
250|              <Ionicons name="chevron-back" size={28} color="#FFFFFF" />
251|            </TouchableOpacity>
252|            <Text style={styles.headerTitle}>Editar Perfil</Text>
253|            <View style={{ width: 28 }} />
254|          </View>
255|
256|          {/* Photos Section */}
257|          <View style={styles.section}>
258|            <Text style={styles.sectionTitle}>Tus fotos ({photos.length}/6)</Text>
259|            <View style={styles.photosGrid}>
260|              {photos.map((photo, index) => (
261|                <View key={index} style={styles.photoContainer}>
262|                  <Image source={{ uri: photo }} style={styles.photo} />
263|                  <TouchableOpacity
264|                    style={styles.removePhotoButton}
265|                    onPress={() => removePhoto(index)}
266|                  >
267|                    <Ionicons name="close-circle" size={24} color="#C41E3A" />
268|                  </TouchableOpacity>
269|                </View>
270|              ))}
271|              {photos.length < 6 && (
272|                <View style={styles.addPhotoButtons}>
273|                  <TouchableOpacity
274|                    style={styles.addPhotoButton}
275|                    onPress={pickImage}
276|                  >
277|                    <Ionicons name="images" size={32} color="#D4AF37" />
278|                    <Text style={styles.addPhotoText}>Galería</Text>
279|                  </TouchableOpacity>
280|                  <TouchableOpacity
281|                    style={styles.addPhotoButton}
282|                    onPress={takePhoto}
283|                  >
284|                    <Ionicons name="camera" size={32} color="#D4AF37" />
285|                    <Text style={styles.addPhotoText}>Cámara</Text>
286|                  </TouchableOpacity>
287|                </View>
288|              )}
289|            </View>
290|          </View>
291|
292|          {/* Basic Info */}
293|          <View style={styles.section}>
294|            <Text style={styles.sectionTitle}>Información básica</Text>
295|            
296|            <Text style={styles.label}>Nombre</Text>
297|            <TextInput
298|              style={styles.input}
299|              value={name}
300|              onChangeText={setName}
301|              placeholder="Tu nombre"
302|              placeholderTextColor="#666666"
303|            />
304|
305|            <Text style={styles.label}>Edad</Text>
306|            <TextInput
307|              style={styles.input}
308|              value={age}
309|              onChangeText={setAge}
310|              placeholder="Tu edad"
311|              placeholderTextColor="#666666"
312|              keyboardType="numeric"
313|              maxLength={2}
314|            />
315|
316|            <Text style={styles.label}>Género</Text>
317|            <View style={styles.optionsRow}>
318|              {genderOptions.map((option) => (
319|                <TouchableOpacity
320|                  key={option.value}
321|                  style={[
322|                    styles.optionButton,
323|                    gender === option.value && styles.optionButtonActive,
324|                  ]}
325|                  onPress={() => setGender(option.value)}
326|                >
327|                  <Text
328|                    style={[
329|                      styles.optionText,
330|                      gender === option.value && styles.optionTextActive,
331|                    ]}
332|                  >
333|                    {option.label}
334|                  </Text>
335|                </TouchableOpacity>
336|              ))}
337|            </View>
338|
339|            <Text style={styles.label}>Buscando</Text>
340|            <View style={styles.optionsRow}>
341|              {lookingForOptions.map((option) => (
342|                <TouchableOpacity
343|                  key={option.value}
344|                  style={[
345|                    styles.optionButton,
346|                    lookingFor === option.value && styles.optionButtonActive,
347|                  ]}
348|                  onPress={() => setLookingFor(option.value)}
349|                >
350|                  <Text
351|                    style={[
352|                      styles.optionText,
353|                      lookingFor === option.value && styles.optionTextActive,
354|                    ]}
355|                  >
356|                    {option.label}
357|                  </Text>
358|                </TouchableOpacity>
359|              ))}
360|            </View>
361|
362|            <Text style={styles.label}>Sobre mí</Text>
363|            <TextInput
364|              style={[styles.input, styles.textArea]}
365|              value={bio}
366|              onChangeText={setBio}
367|              placeholder="Cuéntanos sobre ti..."
368|              placeholderTextColor="#666666"
369|              multiline
370|              maxLength={300}
371|            />
372|          </View>
373|
374|          {/* Location */}
375|          <View style={styles.section}>
376|            <Text style={styles.sectionTitle}>Ubicación</Text>
377|            <View style={styles.locationRow}>
378|              <View style={styles.locationInfo}>
379|                <Ionicons name="location" size={24} color="#D4AF37" />
380|                <Text style={styles.locationText}>
381|                  {city || 'Sin ubicación'}
382|                </Text>
383|              </View>
384|              <TouchableOpacity
385|                style={styles.locationButton}
386|                onPress={updateLocation}
387|                disabled={locationLoading}
388|              >
389|                {locationLoading ? (
390|                  <ActivityIndicator size="small" color="#FFFFFF" />
391|                ) : (
392|                  <Text style={styles.locationButtonText}>Actualizar</Text>
393|                )}
394|              </TouchableOpacity>
395|            </View>
396|          </View>
397|
398|          {/* Verification */}
399|          {!user?.is_verified && (
400|            <View style={styles.section}>
401|              <Text style={styles.sectionTitle}>Verificación</Text>
402|              <TouchableOpacity
403|                style={styles.verifyButton}
404|                onPress={requestVerification}
405|              >
406|                <Ionicons name="shield-checkmark" size={24} color="#D4AF37" />
407|                <View style={styles.verifyButtonContent}>
408|                  <Text style={styles.verifyButtonTitle}>
409|                    Verificar mi perfil
410|                  </Text>
411|                  <Text style={styles.verifyButtonText}>
412|                    Obtén la insignia dorada
413|                  </Text>
414|                </View>
415|              </TouchableOpacity>
416|            </View>
417|          )}
418|
419|          {/* Save Button */}
420|          <TouchableOpacity
421|            style={styles.saveButton}
422|            onPress={saveProfile}
423|            disabled={loading}
424|          >
425|            {loading ? (
426|              <ActivityIndicator color="#FFFFFF" />
427|            ) : (
428|              <Text style={styles.saveButtonText}>Guardar perfil</Text>
429|            )}
430|          </TouchableOpacity>
431|        </ScrollView>
432|      </KeyboardAvoidingView>
433|    </SafeAreaView>
434|  );
435|}
436|
437|const styles = StyleSheet.create({
438|  container: {
439|    flex: 1,
440|    backgroundColor: '#000000',
441|  },
442|  scrollContent: {
443|    paddingBottom: 40,
444|  },
445|  header: {
446|    flexDirection: 'row',
447|    alignItems: 'center',
448|    justifyContent: 'space-between',
449|    padding: 16,
450|  },
451|  backButton: {
452|    padding: 4,
453|  },
454|  headerTitle: {
455|    fontSize: 20,
456|    fontWeight: '600',
457|    color: '#FFFFFF',
458|  },
459|  section: {
460|    padding: 16,
461|    borderBottomWidth: 1,
462|    borderBottomColor: '#222222',
463|  },
464|  sectionTitle: {
465|    fontSize: 18,
466|    fontWeight: '600',
467|    color: '#FFFFFF',
468|    marginBottom: 16,
469|  },
470|  photosGrid: {
471|    flexDirection: 'row',
472|    flexWrap: 'wrap',
473|    gap: 12,
474|  },
475|  photoContainer: {
476|    position: 'relative',
477|  },
478|  photo: {
479|    width: 100,
480|    height: 133,
481|    borderRadius: 12,
482|  },
483|  removePhotoButton: {
484|    position: 'absolute',
485|    top: -8,
486|    right: -8,
487|    backgroundColor: '#000000',
488|    borderRadius: 12,
489|  },
490|  addPhotoButtons: {
491|    flexDirection: 'row',
492|    gap: 12,
493|  },
494|  addPhotoButton: {
495|    width: 100,
496|    height: 133,
497|    borderRadius: 12,
498|    borderWidth: 2,
499|    borderColor: '#333333',
500|    borderStyle: 'dashed',
501|    justifyContent: 'center',
502|    alignItems: 'center',
503|  },
504|  addPhotoText: {
505|    fontSize: 12,
506|    color: '#D4AF37',
507|    marginTop: 8,
508|  },
509|  label: {
510|    fontSize: 14,
511|    color: '#888888',
512|    marginBottom: 8,
513|    marginTop: 16,
514|  },
515|  input: {
516|    backgroundColor: '#1a1a1a',
517|    borderRadius: 12,
518|    padding: 16,
519|    fontSize: 16,
520|    color: '#FFFFFF',
521|    borderWidth: 1,
522|    borderColor: '#333333',
523|  },
524|  textArea: {
525|    height: 100,
526|    textAlignVertical: 'top',
527|  },
528|  optionsRow: {
529|    flexDirection: 'row',
530|    gap: 12,
531|  },
532|  optionButton: {
533|    flex: 1,
534|    paddingVertical: 14,
535|    borderRadius: 12,
536|    backgroundColor: '#1a1a1a',
537|    alignItems: 'center',
538|    borderWidth: 1,
539|    borderColor: '#333333',
540|  },
541|  optionButtonActive: {
542|    backgroundColor: '#C41E3A',
543|    borderColor: '#C41E3A',
544|  },
545|  optionText: {
546|    fontSize: 14,
547|    color: '#888888',
548|  },
549|  optionTextActive: {
550|    color: '#FFFFFF',
551|    fontWeight: '600',
552|  },
553|  locationRow: {
554|    flexDirection: 'row',
555|    alignItems: 'center',
556|    justifyContent: 'space-between',
557|    backgroundColor: '#1a1a1a',
558|    padding: 16,
559|    borderRadius: 12,
560|  },
561|  locationInfo: {
562|    flexDirection: 'row',
563|    alignItems: 'center',
564|    gap: 12,
565|  },
566|  locationText: {
567|    fontSize: 16,
568|    color: '#FFFFFF',
569|  },
570|  locationButton: {
571|    backgroundColor: '#C41E3A',
572|    paddingVertical: 8,
573|    paddingHorizontal: 16,
574|    borderRadius: 20,
575|  },
576|  locationButtonText: {
577|    color: '#FFFFFF',
578|    fontSize: 14,
579|    fontWeight: '600',
580|  },
581|  verifyButton: {
582|    flexDirection: 'row',
583|    alignItems: 'center',
584|    backgroundColor: '#1a1a0a',
585|    padding: 16,
586|    borderRadius: 12,
587|    borderWidth: 1,
588|    borderColor: '#D4AF37',
589|    gap: 12,
590|  },
591|  verifyButtonContent: {
592|    flex: 1,
593|  },
594|  verifyButtonTitle: {
595|    fontSize: 16,
596|    fontWeight: '600',
597|    color: '#D4AF37',
598|  },
599|  verifyButtonText: {
600|    fontSize: 14,
601|    color: '#888888',
602|    marginTop: 2,
603|  },
604|  saveButton: {
605|    backgroundColor: '#C41E3A',
606|    marginHorizontal: 16,
607|    marginTop: 24,
608|    paddingVertical: 16,
609|    borderRadius: 30,
610|    alignItems: 'center',
611|    borderWidth: 2,
612|    borderColor: '#D4AF37',
613|  },
614|  saveButtonText: {
615|    fontSize: 18,
616|    fontWeight: '600',
617|    color: '#FFFFFF',
618|  },
619|});
620|

===END
Y finalmente el backend:
Action: file_editor view /app/backend/server.py
Observation: [Showing lines 1-737 of 737 total] /app/backend/server.py:
1|from fastapi import FastAPI, APIRouter, HTTPException, Request, Response, UploadFile, File, Query, Depends
2|from fastapi.responses import JSONResponse
3|from dotenv import load_dotenv
4|from starlette.middleware.cors import CORSMiddleware
5|from motor.motor_asyncio import AsyncIOMotorClient
6|import os
7|import logging
8|from pathlib import Path
9|from pydantic import BaseModel, Field
10|from typing import List, Optional, Dict, Any
11|import uuid
12|from datetime import datetime, timezone, timedelta
13|import httpx
14|import base64
15|
16|ROOT_DIR = Path(__file__).parent
17|load_dotenv(ROOT_DIR / '.env')
18|
19|# MongoDB connection
20|mongo_url = os.environ['MONGO_URL']
21|client = AsyncIOMotorClient(mongo_url)
22|db = client[os.environ['DB_NAME']]
23|
24|# Create the main app
25|app = FastAPI(title="LH Citas API")
26|
27|# Create a router with the /api prefix
28|api_router = APIRouter(prefix="/api")
29|
30|# Configure logging
31|logging.basicConfig(
32|    level=logging.INFO,
33|    format='%(asctime)s - %(name)s - %(levelname)s - %(message)s'
34|)
35|logger = logging.getLogger(__name__)
36|
37|# ==================== MODELS ====================
38|
39|class UserBase(BaseModel):
40|    email: str
41|    name: str
42|    picture: Optional[str] = None
43|
44|class UserProfile(BaseModel):
45|    user_id: str
46|    email: str
47|    name: str
48|    picture: Optional[str] = None
49|    bio: Optional[str] = None
50|    age: Optional[int] = None
51|    gender: Optional[str] = None
52|    looking_for: Optional[str] = None
53|    photos: List[str] = []
54|    location: Optional[Dict[str, float]] = None  # {lat, lng}
55|    city: Optional[str] = None
56|    is_verified: bool = False
57|    verification_photo: Optional[str] = None
58|    preferences: Optional[Dict[str, Any]] = None
59|    created_at: datetime = Field(default_factory=lambda: datetime.now(timezone.utc))
60|    last_active: datetime = Field(default_factory=lambda: datetime.now(timezone.utc))
61|
62|class ProfileUpdate(BaseModel):
63|    name: Optional[str] = None
64|    bio: Optional[str] = None
65|    age: Optional[int] = None
66|    gender: Optional[str] = None
67|    looking_for: Optional[str] = None
68|    photos: Optional[List[str]] = None
69|    city: Optional[str] = None
70|    preferences: Optional[Dict[str, Any]] = None
71|
72|class LocationUpdate(BaseModel):
73|    latitude: float
74|    longitude: float
75|    city: Optional[str] = None
76|
77|class LikeAction(BaseModel):
78|    target_user_id: str
79|
80|class Message(BaseModel):
81|    id: str = Field(default_factory=lambda: str(uuid.uuid4()))
82|    match_id: str
83|    sender_id: str
84|    content: str
85|    timestamp: datetime = Field(default_factory=lambda: datetime.now(timezone.utc))
86|    read: bool = False
87|
88|class MessageCreate(BaseModel):
89|    content: str
90|
91|class VerificationRequest(BaseModel):
92|    photo: str  # base64 encoded photo
93|
94|# ==================== AUTH HELPERS ====================
95|
96|async def get_current_user(request: Request) -> UserProfile:
97|    """Extract and validate session token from cookie or header"""
98|    session_token = request.cookies.get("session_token")
99|    
100|    if not session_token:
101|        auth_header = request.headers.get("Authorization")
102|        if auth_header and auth_header.startswith("Bearer "):
103|            session_token = auth_header[7:]
104|    
105|    if not session_token:
106|        raise HTTPException(status_code=401, detail="Not authenticated")
107|    
108|    # Find session
109|    session_doc = await db.user_sessions.find_one(
110|        {"session_token": session_token},
111|        {"_id": 0}
112|    )
113|    
114|    if not session_doc:
115|        raise HTTPException(status_code=401, detail="Invalid session")
116|    
117|    # Check expiry
118|    expires_at = session_doc.get("expires_at")
119|    if isinstance(expires_at, str):
120|        expires_at = datetime.fromisoformat(expires_at)
121|    if expires_at.tzinfo is None:
122|        expires_at = expires_at.replace(tzinfo=timezone.utc)
123|    if expires_at < datetime.now(timezone.utc):
124|        raise HTTPException(status_code=401, detail="Session expired")
125|    
126|    # Get user
127|    user_doc = await db.users.find_one(
128|        {"user_id": session_doc["user_id"]},
129|        {"_id": 0}
130|    )
131|    
132|    if not user_doc:
133|        raise HTTPException(status_code=401, detail="User not found")
134|    
135|    # Update last active
136|    await db.users.update_one(
137|        {"user_id": user_doc["user_id"]},
138|        {"$set": {"last_active": datetime.now(timezone.utc)}}
139|    )
140|    
141|    return UserProfile(**user_doc)
142|
143|# ==================== AUTH ENDPOINTS ====================
144|
145|@api_router.post("/auth/session")
146|async def exchange_session(request: Request, response: Response):
147|    """Exchange session_id from Emergent Auth for session_token"""
148|    body = await request.json()
149|    session_id = body.get("session_id")
150|    
151|    if not session_id:
152|        raise HTTPException(status_code=400, detail="session_id required")
153|    
154|    # Exchange session_id with Emergent Auth
155|    async with httpx.AsyncClient() as client_http:
156|        try:
157|            auth_response = await client_http.get(
158|                "https://demobackend.emergentagent.com/auth/v1/env/oauth/session-data",
159|                headers={"X-Session-ID": session_id}
160|            )
161|            
162|            if auth_response.status_code != 200:
163|                logger.error(f"Auth failed: {auth_response.text}")
164|                raise HTTPException(status_code=401, detail="Authentication failed")
165|            
166|            user_data = auth_response.json()
167|        except Exception as e:
168|            logger.error(f"Auth error: {e}")
169|            raise HTTPException(status_code=500, detail="Authentication service error")
170|    
171|    email = user_data.get("email")
172|    name = user_data.get("name")
173|    picture = user_data.get("picture")
174|    session_token = user_data.get("session_token")
175|    
176|    # Check if user exists
177|    existing_user = await db.users.find_one({"email": email}, {"_id": 0})
178|    
179|    if existing_user:
180|        user_id = existing_user["user_id"]
181|        # Update user info
182|        await db.users.update_one(
183|            {"user_id": user_id},
184|            {"$set": {
185|                "name": name,
186|                "picture": picture,
187|                "last_active": datetime.now(timezone.utc)
188|            }}
189|        )
190|    else:
191|        # Create new user
192|        user_id = f"user_{uuid.uuid4().hex[:12]}"
193|        new_user = {
194|            "user_id": user_id,
195|            "email": email,
196|            "name": name,
197|            "picture": picture,
198|            "bio": None,
199|            "age": None,
200|            "gender": None,
201|            "looking_for": None,
202|            "photos": [],
203|            "location": None,
204|            "city": None,
205|            "is_verified": False,
206|            "verification_photo": None,
207|            "preferences": {
208|                "min_age": 18,
209|                "max_age": 50,
210|                "max_distance": 50
211|            },
212|            "created_at": datetime.now(timezone.utc),
213|            "last_active": datetime.now(timezone.utc)
214|        }
215|        await db.users.insert_one(new_user)
216|    
217|    # Store session
218|    expires_at = datetime.now(timezone.utc) + timedelta(days=7)
219|    await db.user_sessions.delete_many({"user_id": user_id})
220|    await db.user_sessions.insert_one({
221|        "user_id": user_id,
222|        "session_token": session_token,
223|        "expires_at": expires_at,
224|        "created_at": datetime.now(timezone.utc)
225|    })
226|    
227|    # Get full user profile
228|    user_doc = await db.users.find_one({"user_id": user_id}, {"_id": 0})
229|    
230|    # Set cookie
231|    response.set_cookie(
232|        key="session_token",
233|        value=session_token,
234|        path="/",
235|        secure=True,
236|        httponly=True,
237|        samesite="none",
238|        max_age=7 * 24 * 60 * 60
239|    )
240|    
241|    return {"user": user_doc}
242|
243|@api_router.get("/auth/me")
244|async def get_me(user: UserProfile = Depends(get_current_user)):
245|    """Get current authenticated user"""
246|    return user.model_dump()
247|
248|@api_router.post("/auth/logout")
249|async def logout(request: Request, response: Response):
250|    """Logout user and clear session"""
251|    session_token = request.cookies.get("session_token")
252|    
253|    if session_token:
254|        await db.user_sessions.delete_many({"session_token": session_token})
255|    
256|    response.delete_cookie(
257|        key="session_token",
258|        path="/",
259|        secure=True,
260|        httponly=True,
261|        samesite="none"
262|    )
263|    
264|    return {"message": "Logged out successfully"}
265|
266|# ==================== PROFILE ENDPOINTS ====================
267|
268|@api_router.put("/profile")
269|async def update_profile(
270|    update: ProfileUpdate,
271|    user: UserProfile = Depends(get_current_user)
272|):
273|    """Update user profile"""
274|    update_data = {k: v for k, v in update.model_dump().items() if v is not None}
275|    update_data["last_active"] = datetime.now(timezone.utc)
276|    
277|    await db.users.update_one(
278|        {"user_id": user.user_id},
279|        {"$set": update_data}
280|    )
281|    
282|    updated_user = await db.users.find_one({"user_id": user.user_id}, {"_id": 0})
283|    return updated_user
284|
285|@api_router.put("/profile/location")
286|async def update_location(
287|    location: LocationUpdate,
288|    user: UserProfile = Depends(get_current_user)
289|):
290|    """Update user location"""
291|    await db.users.update_one(
292|        {"user_id": user.user_id},
293|        {"$set": {
294|            "location": {"lat": location.latitude, "lng": location.longitude},
295|            "city": location.city,
296|            "last_active": datetime.now(timezone.utc)
297|        }}
298|    )
299|    
300|    return {"message": "Location updated"}
301|
302|@api_router.post("/profile/photos")
303|async def add_photo(
304|    request: Request,
305|    user: UserProfile = Depends(get_current_user)
306|):
307|    """Add a photo to profile (base64)"""
308|    body = await request.json()
309|    photo_base64 = body.get("photo")
310|    
311|    if not photo_base64:
312|        raise HTTPException(status_code=400, detail="Photo required")
313|    
314|    # Limit to 6 photos
315|    current_photos = user.photos or []
316|    if len(current_photos) >= 6:
317|        raise HTTPException(status_code=400, detail="Maximum 6 photos allowed")
318|    
319|    current_photos.append(photo_base64)
320|    
321|    await db.users.update_one(
322|        {"user_id": user.user_id},
323|        {"$set": {"photos": current_photos}}
324|    )
325|    
326|    return {"message": "Photo added", "photos": current_photos}
327|
328|@api_router.delete("/profile/photos/{photo_index}")
329|async def delete_photo(
330|    photo_index: int,
331|    user: UserProfile = Depends(get_current_user)
332|):
333|    """Delete a photo from profile"""
334|    current_photos = user.photos or []
335|    
336|    if photo_index < 0 or photo_index >= len(current_photos):
337|        raise HTTPException(status_code=400, detail="Invalid photo index")
338|    
339|    current_photos.pop(photo_index)
340|    
341|    await db.users.update_one(
342|        {"user_id": user.user_id},
343|        {"$set": {"photos": current_photos}}
344|    )
345|    
346|    return {"message": "Photo deleted", "photos": current_photos}
347|
348|# ==================== VERIFICATION ENDPOINTS ====================
349|
350|@api_router.post("/profile/verify")
351|async def request_verification(
352|    request: Request,
353|    user: UserProfile = Depends(get_current_user)
354|):
355|    """Request photo verification"""
356|    body = await request.json()
357|    verification_photo = body.get("photo")
358|    
359|    if not verification_photo:
360|        raise HTTPException(status_code=400, detail="Verification photo required")
361|    
362|    # Store verification request
363|    await db.verification_requests.insert_one({
364|        "id": str(uuid.uuid4()),
365|        "user_id": user.user_id,
366|        "photo": verification_photo,
367|        "status": "pending",
368|        "created_at": datetime.now(timezone.utc)
369|    })
370|    
371|    # For MVP, auto-approve verification
372|    await db.users.update_one(
373|        {"user_id": user.user_id},
374|        {"$set": {
375|            "is_verified": True,
376|            "verification_photo": verification_photo
377|        }}
378|    )
379|    
380|    return {"message": "Verification approved", "is_verified": True}
381|
382|# ==================== DISCOVERY ENDPOINTS ====================
383|
384|@api_router.get("/discover")
385|async def discover_profiles(
386|    user: UserProfile = Depends(get_current_user),
387|    min_age: int = Query(18, ge=18),
388|    max_age: int = Query(99, le=99),
389|    max_distance: int = Query(100, ge=1)
390|):
391|    """Get profiles to discover (excluding already liked/matched)"""
392|    # Get users I've already liked
393|    my_likes = await db.likes.find({"from_user": user.user_id}).to_list(1000)
394|    liked_user_ids = [like["to_user"] for like in my_likes]
395|    
396|    # Get my matches
397|    my_matches = await db.matches.find({
398|        "$or": [
399|            {"user1_id": user.user_id},
400|            {"user2_id": user.user_id}
401|        ]
402|    }).to_list(1000)
403|    matched_user_ids = []
404|    for match in my_matches:
405|        if match["user1_id"] == user.user_id:
406|            matched_user_ids.append(match["user2_id"])
407|        else:
408|            matched_user_ids.append(match["user1_id"])
409|    
410|    # Exclude me, liked users, and matched users
411|    excluded_ids = [user.user_id] + liked_user_ids + matched_user_ids
412|    
413|    # Build query
414|    query = {
415|        "user_id": {"$nin": excluded_ids},
416|        "photos": {"$exists": True, "$ne": []},
417|        "age": {"$gte": min_age, "$lte": max_age}
418|    }
419|    
420|    # Apply gender filter
421|    if user.looking_for and user.looking_for != "todos":
422|        query["gender"] = user.looking_for
423|    
424|    # Get profiles
425|    profiles = await db.users.find(query, {"_id": 0}).to_list(50)
426|    
427|    # If user has location, calculate distances (simplified)
428|    if user.location:
429|        for profile in profiles:
430|            if profile.get("location"):
431|                # Simple distance calculation (not precise, but good for MVP)
432|                lat_diff = abs(user.location["lat"] - profile["location"]["lat"])
433|                lng_diff = abs(user.location["lng"] - profile["location"]["lng"])
434|                # Rough km estimate
435|                distance = ((lat_diff ** 2 + lng_diff ** 2) ** 0.5) * 111
436|                profile["distance"] = round(distance, 1)
437|            else:
438|                profile["distance"] = None
439|        
440|        # Filter by distance if specified
441|        if max_distance < 100:
442|            profiles = [p for p in profiles if p.get("distance") is None or p["distance"] <= max_distance]
443|    
444|    return profiles
445|
446|@api_router.get("/profile/{user_id}")
447|async def get_profile(
448|    user_id: str,
449|    user: UserProfile = Depends(get_current_user)
450|):
451|    """Get a specific user profile"""
452|    profile = await db.users.find_one({"user_id": user_id}, {"_id": 0})
453|    
454|    if not profile:
455|        raise HTTPException(status_code=404, detail="User not found")
456|    
457|    return profile
458|
459|# ==================== LIKE/MATCH ENDPOINTS ====================
460|
461|@api_router.post("/like")
462|async def like_user(
463|    action: LikeAction,
464|    user: UserProfile = Depends(get_current_user)
465|):
466|    """Like a user - creates a match if mutual"""
467|    target_user_id = action.target_user_id
468|    
469|    if target_user_id == user.user_id:
470|        raise HTTPException(status_code=400, detail="Cannot like yourself")
471|    
472|    # Check if target user exists
473|    target_user = await db.users.find_one({"user_id": target_user_id}, {"_id": 0})
474|    if not target_user:
475|        raise HTTPException(status_code=404, detail="User not found")
476|    
477|    # Check if already liked
478|    existing_like = await db.likes.find_one({
479|        "from_user": user.user_id,
480|        "to_user": target_user_id
481|    })
482|    
483|    if existing_like:
484|        return {"message": "Already liked", "is_match": False}
485|    
486|    # Create like
487|    await db.likes.insert_one({
488|        "id": str(uuid.uuid4()),
489|        "from_user": user.user_id,
490|        "to_user": target_user_id,
491|        "created_at": datetime.now(timezone.utc)
492|    })
493|    
494|    # Check if mutual like (match!)
495|    mutual_like = await db.likes.find_one({
496|        "from_user": target_user_id,
497|        "to_user": user.user_id
498|    })
499|    
500|    is_match = False
501|    match_data = None
502|    
503|    if mutual_like:
504|        is_match = True
505|        # Create match
506|        match_id = str(uuid.uuid4())
507|        created_at = datetime.now(timezone.utc)
508|        match_data = {
509|            "match_id": match_id,
510|            "user1_id": user.user_id,
511|            "user2_id": target_user_id,
512|            "created_at": created_at
513|        }
514|        await db.matches.insert_one(match_data)
515|        
516|        # Add matched user info (ensure proper serialization by creating clean dict)
517|        clean_target_user = {
518|            "user_id": target_user.get("user_id"),
519|            "name": target_user.get("name"),
520|            "age": target_user.get("age"),
521|            "photos": target_user.get("photos", []),
522|            "bio": target_user.get("bio"),
523|            "city": target_user.get("city"),
524|            "is_verified": target_user.get("is_verified", False)
525|        }
526|        # Return serializable match data
527|        match_data = {
528|            "match_id": match_id,
529|            "user1_id": user.user_id,
530|            "user2_id": target_user_id,
531|            "created_at": created_at.isoformat(),
532|            "matched_user": clean_target_user
533|        }
534|    
535|    return {
536|        "message": "It's a match!" if is_match else "Liked",
537|        "is_match": is_match,
538|        "match": match_data
539|    }
540|
541|@api_router.post("/pass")
542|async def pass_user(
543|    action: LikeAction,
544|    user: UserProfile = Depends(get_current_user)
545|):
546|    """Pass on a user (don't like)"""
547|    # Record the pass to exclude from future discovery
548|    await db.passes.insert_one({
549|        "id": str(uuid.uuid4()),
550|        "from_user": user.user_id,
551|        "to_user": action.target_user_id,
552|        "created_at": datetime.now(timezone.utc)
553|    })
554|    
555|    return {"message": "Passed"}
556|
557|@api_router.get("/matches")
558|async def get_matches(user: UserProfile = Depends(get_current_user)):
559|    """Get all matches for current user"""
560|    matches = await db.matches.find({
561|        "$or": [
562|            {"user1_id": user.user_id},
563|            {"user2_id": user.user_id}
564|        ]
565|    }, {"_id": 0}).to_list(100)
566|    
567|    # Enrich with user info and last message
568|    result = []
569|    for match in matches:
570|        other_user_id = match["user2_id"] if match["user1_id"] == user.user_id else match["user1_id"]
571|        other_user = await db.users.find_one({"user_id": other_user_id}, {"_id": 0})
572|        
573|        if other_user:
574|            # Get last message
575|            last_message = await db.messages.find_one(
576|                {"match_id": match["match_id"]},
577|                {"_id": 0},
578|                sort=[("timestamp", -1)]
579|            )
580|            
581|            # Count unread messages
582|            unread_count = await db.messages.count_documents({
583|                "match_id": match["match_id"],
584|                "sender_id": other_user_id,
585|                "read": False
586|            })
587|            
588|            result.append({
589|                "match_id": match["match_id"],
590|                "user": other_user,
591|                "last_message": last_message,
592|                "unread_count": unread_count,
593|                "created_at": match["created_at"]
594|            })
595|    
596|    # Sort by last message or match date
597|    result.sort(
598|        key=lambda x: x["last_message"]["timestamp"] if x["last_message"] else x["created_at"],
599|        reverse=True
600|    )
601|    
602|    return result
603|
604|@api_router.get("/likes/received")
605|async def get_received_likes(user: UserProfile = Depends(get_current_user)):
606|    """Get users who have liked me (but I haven't liked back)"""
607|    # Get my likes
608|    my_likes = await db.likes.find({"from_user": user.user_id}).to_list(1000)
609|    users_i_liked = [like["to_user"] for like in my_likes]
610|    
611|    # Get likes to me that I haven't reciprocated
612|    received_likes = await db.likes.find({
613|        "to_user": user.user_id,
614|        "from_user": {"$nin": users_i_liked}
615|    }).to_list(100)
616|    
617|    # Get user info
618|    result = []
619|    for like in received_likes:
620|        liker = await db.users.find_one({"user_id": like["from_user"]}, {"_id": 0})
621|        if liker:
622|            result.append({
623|                "user": liker,
624|                "liked_at": like["created_at"]
625|            })
626|    
627|    return result
628|
629|# ==================== CHAT ENDPOINTS ====================
630|
631|@api_router.get("/chat/{match_id}")
632|async def get_chat_messages(
633|    match_id: str,
634|    user: UserProfile = Depends(get_current_user)
635|):
636|    """Get messages for a match"""
637|    # Verify user is part of this match
638|    match = await db.matches.find_one({
639|        "match_id": match_id,
640|        "$or": [
641|            {"user1_id": user.user_id},
642|            {"user2_id": user.user_id}
643|        ]
644|    })
645|    
646|    if not match:
647|        raise HTTPException(status_code=404, detail="Match not found")
648|    
649|    # Get messages
650|    messages = await db.messages.find(
651|        {"match_id": match_id},
652|        {"_id": 0}
653|    ).sort("timestamp", 1).to_list(500)
654|    
655|    # Mark messages as read
656|    other_user_id = match["user2_id"] if match["user1_id"] == user.user_id else match["user1_id"]
657|    await db.messages.update_many(
658|        {"match_id": match_id, "sender_id": other_user_id, "read": False},
659|        {"$set": {"read": True}}
660|    )
661|    
662|    # Get other user info
663|    other_user = await db.users.find_one({"user_id": other_user_id}, {"_id": 0})
664|    
665|    return {
666|        "match_id": match_id,
667|        "other_user": other_user,
668|        "messages": messages
669|    }
670|
671|@api_router.post("/chat/{match_id}")
672|async def send_message(
673|    match_id: str,
674|    message: MessageCreate,
675|    user: UserProfile = Depends(get_current_user)
676|):
677|    """Send a message in a match chat"""
678|    # Verify user is part of this match
679|    match = await db.matches.find_one({
680|        "match_id": match_id,
681|        "$or": [
682|            {"user1_id": user.user_id},
683|            {"user2_id": user.user_id}
684|        ]
685|    })
686|    
687|    if not match:
688|        raise HTTPException(status_code=404, detail="Match not found")
689|    
690|    # Create message
691|    timestamp = datetime.now(timezone.utc)
692|    new_message = {
693|        "id": str(uuid.uuid4()),
694|        "match_id": match_id,
695|        "sender_id": user.user_id,
696|        "content": message.content,
697|        "timestamp": timestamp,
698|        "read": False
699|    }
700|    
701|    await db.messages.insert_one(new_message)
702|    
703|    # Return serializable message
704|    return {
705|        "id": new_message["id"],
706|        "match_id": match_id,
707|        "sender_id": user.user_id,
708|        "content": message.content,
709|        "timestamp": timestamp.isoformat(),
710|        "read": False
711|    }
712|
713|# ==================== STATUS ENDPOINT ====================
714|
715|@api_router.get("/")
716|async def root():
717|    return {"message": "LH Citas API", "status": "running"}
718|
719|@api_router.get("/health")
720|async def health():
721|    return {"status": "healthy"}
722|
723|# Include the router in the main app
724|app.include_router(api_router)
725|
726|app.add_middleware(
727|    CORSMiddleware,
728|    allow_credentials=True,
729|    allow_origins=["*"],
730|    allow_methods=["*"],
731|    allow_headers=["*"],
732|)
733|
734|@app.on_event("shutdown")
735|async def shutdown_db_client():
736|    client.close()
737|
[End of file]
