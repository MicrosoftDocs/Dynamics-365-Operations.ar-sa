---
title: ارتباط تسجيل الدخول يقوم بإعادة التوجيه مرة أخرى إلى موقع التجارة الإلكترونية
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة قيام ارتباط تسجيل الدخول بإعادة التوجيه إلى موقع التجارة الإلكترونية بدلا من الانتقال إلى صفحة تسجيل الدخول.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a1d0ae4e487c391020947c607d5d7cb5d1ba6af4
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020593"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a><span data-ttu-id="d057a-103">ارتباط تسجيل الدخول يقوم بإعادة التوجيه مرة أخرى إلى موقع التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="d057a-103">Sign-in link redirects back to an e-commerce site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d057a-104">يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة قيام ارتباط تسجيل الدخول بإعادة التوجيه إلى موقع التجارة الإلكترونية بدلا من الانتقال إلى صفحة تسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="d057a-104">This topic provides troubleshooting guidance that can help when a sign-in link redirects back to the e-commerce site instead of going to the sign-in page.</span></span>

## <a name="description"></a><span data-ttu-id="d057a-105">الوصف</span><span class="sxs-lookup"><span data-stu-id="d057a-105">Description</span></span>

<span data-ttu-id="d057a-106">بعد تكوين مستأجر جديد لـ B2C في Microsoft Azure Active Directory (B2C لـ Azure AD) في منشئ مواقع Commerce، تتم إعادة توجيه المستخدمين الذين يقومون بتحديد ارتباط **تسجيل الدخول** مرة أخرى إلى الصفحة المنتقل إليها الرئيسية للتجارة الإلكترونية دون الانتقال إلى صفحه تسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="d057a-106">After you configure a new Microsoft Azure Active Directory B2C (Azure AD B2C) tenant in Commerce site builder, users who select the **Sign in** link are redirected back to the main e-commerce landing page without going to the sign-in page.</span></span>

## <a name="resolution"></a><span data-ttu-id="d057a-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="d057a-107">Resolution</span></span>

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a><span data-ttu-id="d057a-108">التأكد من تكوين عنوان URL للرد بشكل صحيح في تطبيق B2C لـ Azure AD</span><span class="sxs-lookup"><span data-stu-id="d057a-108">Confirm that the reply URL is correctly configured in the Azure AD B2C application</span></span>

<span data-ttu-id="d057a-109">لتأكد من تكوين عنوان URL للرد بشكل صحيح في تطبيق B2C لـ Azure AD، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="d057a-109">To confirm that the reply URL is correctly configured in the Azure AD B2C application, follow these steps.</span></span>

1. <span data-ttu-id="d057a-110">انتقل إلى [مدخل Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="d057a-110">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="d057a-111">حدد تطبيق B2C لـ Azure AD الذي قمت بإنشائه للوصول إلى الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="d057a-111">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="d057a-112">حدد التطبيق الذي قمت بإنشائه أثناء إعداد B2C لـ Azure AD.</span><span class="sxs-lookup"><span data-stu-id="d057a-112">Select the application that you created during the Azure AD B2C setup.</span></span>
1. <span data-ttu-id="d057a-113">تحت **عنوان URL للرد**، تأكد من أن القائمة تتضمن إدخالات لكل من عنوان URL لمجال الموقع وعنوان URL الذي تم إنشاؤه بواسطة التجارة الإلكترونية، كما هو موضح في المثال الموجود في التوضيح التالي.</span><span class="sxs-lookup"><span data-stu-id="d057a-113">Under **Reply URL**, make sure that the list includes entries for both the site domain URL and the e-commerce-generated URL, as shown in the example in the following illustration.</span></span>

    ![إدخالات URL للرد الخاصة بـ B2C لـ Azure AD](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> <span data-ttu-id="d057a-115">يجب أن يكون كل من عنوان URL لمجال الموقع وعنوان URL المنشأ بواسطة التجارة الإلكترونية بتنسيق URL صالح لا يحتوي على خطوط مائلة سابقة أو لاحقة.</span><span class="sxs-lookup"><span data-stu-id="d057a-115">Both the site domain URL and the e-commerce-generated URL must be in a valid URL format that doesn't include leading or trailing slashes.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d057a-116">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d057a-116">Additional resources</span></span>

[<span data-ttu-id="d057a-117">تسجيل تطبيق ويب في B2C لـ Azure Active Directory </span><span class="sxs-lookup"><span data-stu-id="d057a-117">Register a web application in Azure Active Directory B2C</span></span>](/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[<span data-ttu-id="d057a-118">إعداد مستأجر متاجرة عمل-مستهلك في Commerce</span><span class="sxs-lookup"><span data-stu-id="d057a-118">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)