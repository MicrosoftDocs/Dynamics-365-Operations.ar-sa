---
title: لا يمكنك تطبيق قالب على منتج تم إصداره
description: لا يمكنك تطبيق قالب على منتج تم إصداره.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ad6efdced9bce924fbf5bc207c92fa2c3a6c79d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026228"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a><span data-ttu-id="7319c-103">لا يمكنك تطبيق قالب لإنشاء منتج تم إصداره</span><span class="sxs-lookup"><span data-stu-id="7319c-103">You can't apply a template to create a released product</span></span>

<span data-ttu-id="7319c-104">رقم KB: 4612097</span><span class="sxs-lookup"><span data-stu-id="7319c-104">KB number: 4612097</span></span>

## <a name="symptoms"></a><span data-ttu-id="7319c-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="7319c-105">Symptoms</span></span>

<span data-ttu-id="7319c-106">عند إنشاء منتج جديد تم إصداره باستخدام مربع الحوار **منتج صادر جديد‬‏‫**، يمكنك تحديد قالب.</span><span class="sxs-lookup"><span data-stu-id="7319c-106">When you create a new released product by using the **New released product** dialog box, you can select a template.</span></span> <span data-ttu-id="7319c-107">ويجب أن يوفر القالب الإعدادات الافتراضية للعديد من الحقول للمنتج الجديد الذي تم إصداره.</span><span class="sxs-lookup"><span data-stu-id="7319c-107">The template is supposed to provide default settings for many fields of the new released product.</span></span> <span data-ttu-id="7319c-108">ومع ذلك، لا يتم تعيين بعض أو كافة الحقول بعد تحديد القالب.</span><span class="sxs-lookup"><span data-stu-id="7319c-108">However, some or all of the fields aren't set after you select the template.</span></span>

## <a name="cause"></a><span data-ttu-id="7319c-109">السبب</span><span class="sxs-lookup"><span data-stu-id="7319c-109">Cause</span></span>

<span data-ttu-id="7319c-110">تتيح لك العديد من الصفحات في Microsoft Dynamics 365 Supply Chain Management إنشاء قالب يقوم بتأسيس الإعدادات الأولية للسجلات التي تظهر في تلك الصفحات.</span><span class="sxs-lookup"><span data-stu-id="7319c-110">Many pages in Microsoft Dynamics 365 Supply Chain Management let you create a template that establishes initial settings for the records that are shown on those pages.</span></span> <span data-ttu-id="7319c-111">يمكنك إنشاء أحد هذه القوالب من خلال تحديد **تسجيل المعلومات** في علامة التبويب **خيارات** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="7319c-111">You can create one of these templates by selecting **Record info** on the **Options** tab of the Action Pane.</span></span> <span data-ttu-id="7319c-112">ومع ذلك، فإن المنتجات التي تم إصدارها تكون معقدة أكثر بكثير من معظم أنواع السجلات الأخرى.</span><span class="sxs-lookup"><span data-stu-id="7319c-112">However, released products are much more complex than most other types of records.</span></span> <span data-ttu-id="7319c-113">على الرغم من أنه يمكنك تحديد **معلومات السجل** على الصفحة **المنتجات التي تم إصدارها** لإنشاء قالب، وعلى الرغم من أنه يمكنك تحديد القالب عند إنشاء منتج تم إصداره، فلن يوفر القالب قيم الحقل المتوقعة للمنتج الجديد الذي تم إصداره.</span><span class="sxs-lookup"><span data-stu-id="7319c-113">Although you can select **Record info** on the **Released products** page to create a template, and although you can select that template when you create a released product, the template won't provide the expected field values for the new released product.</span></span> <span data-ttu-id="7319c-114">لذلك، لا يمكنك استخدام قوالب "معلومات السجل" للمنتجات التي تم إصدارها.</span><span class="sxs-lookup"><span data-stu-id="7319c-114">Therefore, you can't use "record info" templates for released products.</span></span> <span data-ttu-id="7319c-115">وبدلاً من ذلك، يجب إنشاء قوالب منتجات مخصصة.</span><span class="sxs-lookup"><span data-stu-id="7319c-115">Instead, you must create dedicated product templates.</span></span>

## <a name="resolution"></a><span data-ttu-id="7319c-116">الدقة</span><span class="sxs-lookup"><span data-stu-id="7319c-116">Resolution</span></span>

<span data-ttu-id="7319c-117">لإنشاء قالب منتج، استخدم القائمة **قالب** في علامة التبويب **المنتج** في جزء الإجراء، وليس الزر **معلومات السجل** في علامة التبويب **خيارات**.</span><span class="sxs-lookup"><span data-stu-id="7319c-117">To create a product template, use the **Template** menu on the **Product** tab of the Action Pane, not the **Record info** button on the **Options** tab.</span></span>

1. <span data-ttu-id="7319c-118">انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="7319c-118">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="7319c-119">في جزء الإجراء، ضمن علامة التبويب **المنتج**، في المجموعة **جديد**، حدد **القالب**، ثم حدد إما **إنشاء قالب شخصي** أو **إنشاء قالب مشترك**، كما هو مناسب.</span><span class="sxs-lookup"><span data-stu-id="7319c-119">On the Action Pane, on the **Product** tab, in the **New** group, select **Template**, and then select either **Create personal template** or **Create shared template**, as appropriate.</span></span>
